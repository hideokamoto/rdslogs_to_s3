## Serverless Framework AWS Lambda function to export Amazon RDS MySQL Query Logs to S3
Serverless Framework for [AWS Lambda function to export Amazon RDS MySQL Query Logs to S3](https://github.com/ryanholland/rdslogs_to_s3) .

## Requirments
- Serverless Framework v1.0.0 or later

## Setup

### clone it

```
$ git clone git@github.com:hideokamoto/rdslogs_to_s3.git
```
### Set ENV Parameter

```
$ export FUNC_PREFIX=sample
```

### configure Lambda function

set following parameters in Lambda function(rdslogs/rds_mysql_to_s3.py)

```
S3BCUKET='rds-mysql-logs-sample'
S3PREFIX='[Prefix to use within the specified bucket]/'
RDSINSANCE='[RDS DB Instance Name]'
LOGNAME='general/mysql-general'
LASTRECIEVED='lastWrittenMarker'
REGION='[RegionName]'
```
`S3BCUKET` should be `rds-mysql-logs-` + `FUNC_PREFIX`.

### Deploy

```
$ sls deploy -r [RegionName]
```
