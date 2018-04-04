### rain-animator

(work in progress - probably not usuable atm)

Dynamically create gif/mp4 animations of rain radar data

Dependencies
- rain-collector stack (for data bucket where all the rain and layer images come from)
- rainradar-config stack (where the config for enabled radars comes from)

Cloudformation
- deploy cloudformation stack
- parameter descriptions should be enough of a clue for what to fill in

#### Upload Lambas to S3

Upload lambdas to S3 so they can be referenced by Lambda for example:

```
#create a bucket
aws s3 mb s3://my-lambdas-bucket

#upload pre-built lambdas
aws s3 cp ./lambda_functions/builds/Animation-1.0-SNAPSHOT.jar  s3://my-lambdas-bucket
aws s3 cp ./lambda_functions/builds/Assistant-1.0-SNAPSHOT.jar  s3://my-lambdas-bucket
```

