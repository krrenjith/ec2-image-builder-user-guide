# Use cron expressions in EC2 Image Builder<a name="cron-expressions"></a>

Use cron expressions for EC2 Image Builder to set up a time window to refresh your image with updates that apply to your pipeline's source image and components\. The time window for your pipeline refresh starts with the time you set in the cron expression\. Your pipeline build can run on or after the start time\.

It can sometimes take up to an hour for your build to start running\.

**Note**  
Cron expressions use Universal Coordinated Time \(UTC\)\. For more information about UTC time, and to find the offset for your time zone, see [Time Zone Abbreviations – Worldwide List](https://www.timeanddate.com/time/zones/)\.

## Supported values for cron expressions in Image Builder<a name="ib-cron-support"></a>

EC2 Image Builder uses the traditional cron format, which consists of five required fields\. Each one is separated from the others by a space in between, with no leading or trailing spaces:

`<Minutes> <Hour> <Day> <Month> <Day of the week>`

Some wildcards are not supported for pipeline builds\. For example, the frequency of pipeline builds is limited to once per 24\-hour period\. Therefore, wildcards that result in more than one build a day are not supported\.

The following table shows supported values for required cron entries\.


**Supported values for cron expressions**  

| Field | Values | Wildcards | 
| --- | --- | --- | 
| Minutes | 0\-59 | not supported | 
| Hour | 0\-23 | not supported | 
| Day | 1\-31 | \- \* / L | 
| Month | 1\-12 or jan\-dec | , \- \* / | 
| Day of the week | 1\-7 or mon\-sun | , \- \* / L \# | 

**Wildcards**  
The following table describes how Image Builder uses wildcards for cron expressions\. Wildcards are not permitted in time fields\. You must specify a fixed time in hours and minutes that will initiate your pipeline build\. Keep in mind that it can take up to an hour after the time you specify for the build to start\.


**Supported wildcards for cron expressions**  

| Wildcard | Description | 
| --- | --- | 
| , | The , \(comma\) wildcard includes additional values\. In the Month field, jan,feb,mar includes January, February, and March\. | 
| \- | The \- \(dash\) wildcard specifies ranges\. In the day of the month field, 1\-15 includes days 1 through 15 of the specified month\. | 
| \* | The \* \(asterisk\) wildcard includes all valid values for the field\.  | 
| / | The / \(forward slash\) wildcard specifies increments\. For example, if you want your build to run every other day, enter \*/2 in the day field\. | 
| L | The L wildcard in either of the day fields, specifies the last day: 28\-31 for the day of the month, depending on what the month is, or Sunday, for the day of the week\. | 
| \# | The \# \(hash\) is allowed only for the day of the week field, and must be followed by a number between 1 and 5\. The number specifies which weeks in a given month apply for the build to run\. For example, if you want your build to run on the second Friday of each month, use fri\#2 for the day of the week field\. If you want your job to run twice a month, on the second and fourth Saturday of the month, you would use sat\#2,4 for the day of the week field\. | 

## Examples of cron expressions in EC2 Image Builder<a name="ib-cron-examples"></a>

Cron expressions are entered differently for the Image Builder console, than they are for the API or CLI\. To see examples, choose the tab that applies to you\.

------
#### [ Image Builder console ]

The following examples show cron expressions that you can enter into the console for your build schedule\.

**Run daily at 10:00 \(UTC\)**  
`0 10 * * *`

**Run daily at midnight \(UTC\)**  
0 0 \* \* \*

**Run at 10:00 \(UTC\) every weekday morning**  
`0 10 * * 1-5`

**Run at 18:00 \(UTC\) every weekday evening**  
`0 18 * * mon-fri`

**Run at 8:00 \(UTC\) on the first day of every month**  
0 8 1 \* \*

**Run on the second Tuesday of every month at 22:30 \(UTC\)**  
30 22 \* \* tue\#2

**Tip**  
If you don't want your pipeline job to extend into the next day while it's running, make sure that your build window start time is at least an hour before midnight\.

------
#### [ API/CLI ]

The following examples show cron expressions that you can enter for your build schedule using CLI commands or API requests\. Only the cron expression is shown\.

**Run daily at 10:00 \(UTC\)**  
`cron(0 10 * * *)`

**Run daily at midnight \(UTC\)**  
cron\(0 0 \* \* \*\)

**Run at 10:00 \(UTC\) every weekday morning**  
`cron(0 10 * * 1-5)`

**Run at 18:00 \(UTC\) every weekday evening**  
`cron(0 18 * * mon-fri)`

**Run at 8:00 \(UTC\) on the first day of every month**  
cron\(0 8 1 \* \*\)

**Run on the second Tuesday of every month at 22:30 \(UTC\)**  
cron\(30 22 \* \* tue\#2\)

**Tip**  
If you don't want your pipeline job to extend into the next day while it's running, allow enough time for your build window\.

------