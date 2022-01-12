# Connection Parameter Specification

## Generic

Keys that are applicable for all services.

| Key      | Default | Example |
|----------|---------|---------|
| `useSsl` | `true`  | `false` |

## AWS

Keys for connecting to AWS services.

| Key                  | Default        | Example                |
|----------------------|----------------|------------------------|
| `awsAccessKeyId`     |                | `ABCDABCDABCDABCD1234` |
| `awsSecretAccessKey` |                |                        |
| `awsSessionToken`    |                |                        |
| `awsRegion`          |                | `eu-central-1`         |
| `awsEndpointOverride`| _AWS endpoint_ | `s3.my-company.de`     |

### S3

Keys for connecting to AWS S3.

| Key                 | Default | Example        |
|---------------------|---------|----------------|
| `s3Bucket`          |         | `my-s3-bucket` |
| `s3PathStyleAccess` | `false` | `true`         |
