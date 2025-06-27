# we can use either one or both  “aws-java-sdk” from maven or"spring-cloud-starter-aw"
```
<dependency>
				<groupId>org.springframework.cloud</groupId>
				<artifactId>spring-cloud-starter-aws</artifactId>
			</dependency>

			<dependency>
				<groupId>com.fasterxml.jackson.core</groupId>
				<artifactId>jackson-databind</artifactId>
				<version>2.15.3</version> <!-- or latest -->
			</dependency>


			<!-- https://mvnrepository.com/artifact/com.amazonaws/aws-java-sdk -->
			<dependency>
				<groupId>com.amazonaws</groupId>
				<artifactId>aws-java-sdk</artifactId>
				<version>1.12.775</version>
			</dependency>
 ```

# export credential via commandline 
```
export AWS_ACCESS_KEY_ID=xxx
export AWS_SECRET_ACCESS_KEY=xxx
export AWS_REGION=us-east-1

```

✅ Example of ~/.aws/credentials file:

[dev]

aws_access_key_id = YOUR_DEV_ACCESS_KEY

aws_secret_access_key = YOUR_DEV_SECRET_KEY

✅ Example of ~/.aws/config file:
```
[default]
region = us-east-1
```

