# Connection Parameter Specification

## Generic

We define the connection information as JSON. The JSON is embedded into the `IDENTIFIED BY` part of the connection definition. The `TO` and `USER` fields must be empty.

Example:

```sql
CREATE OR REPLACE CONNECTION S3_CONNECTION
TO ''
USER ''
IDENTIFIED BY '{
  "awsAccessKeyId": "<AWS_ACCESS_KEY>",
  "awsSecretAccessKey": "<AWS_SECRET_KEY>",
  "awsRegion": "<SESSION_TOKEN>",
  "s3Bucket": "<BUCKET_NAME>"
}';
```

For the future it's planned to replace this by an adapted SQL syntax that only accepts the JSON string.

Keys that are applicable for all services.

| Key      | Json Type | Default | Example |
|----------|-----------|---------|---------|
| `useSsl` | bool      | `true`  | `false` |

## AWS

Keys for connecting to AWS services.

| Key                   | Json Type | Default        | Example                  |
|-----------------------|-----------|----------------|--------------------------|
| `awsAccessKeyId`      | string    |                | `"ABCDABCDABCDABCD1234"` |
| `awsSecretAccessKey`  | string    |                |                          |
| `awsSessionToken`     | string    |                |                          |
| `awsRegion`           | string    |                | `"eu-central-1"`         |
| `awsEndpointOverride` | string    | _AWS endpoint_ | `"s3.my-company.de"`     |

### S3

Keys for connecting to AWS S3.

| Key                 | Json Type | Default | Example          |
|---------------------|-----------|---------|------------------|
| `s3Bucket`          | string    |         | `"my-s3-bucket"` |
| `s3PathStyleAccess` | bool      | `false` | `true`           |
