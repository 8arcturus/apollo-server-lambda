_Reference:_ https://github.com/apollographql/apollo-server/tree/master/packages/apollo-server-lambda

`npm install apollo-server-lambda graphql`

```
 aws cloudformation package \
  --template-file template.yaml \
  --output-template-file serverless-output.yaml \
  --s3-bucket ssr-apollo-server-lambda-2 --profile <AWS_PROFILE_NAME>
```

```
aws cloudformation deploy \
  --template-file serverless-output.yaml \
  --stack-name prod \
  --capabilities CAPABILITY_IAM --profile <AWS_PROFILE_NAME>
```


