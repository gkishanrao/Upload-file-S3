# we can use either one or both  “aws-java-sdk” from maven or"spring-cloud-starter-aw"

✅ 1. Spring Cloud AWS Starter
```
<dependency>
    <groupId>org.springframework.cloud</groupId>
    <artifactId>spring-cloud-starter-aws</artifactId>
</dependency>
```
# Purpose: Simplifies AWS service integration (like S3, SNS, SQS) in Spring Boot.

# Note: Make sure you're also including the correct Spring Cloud BOM for version alignment, e.g.:

```
<dependencyManagement>
    <dependencies>
        <dependency>
            <groupId>org.springframework.cloud</groupId>
            <artifactId>spring-cloud-dependencies</artifactId>
            <version>Hoxton.SR12</version> <!-- Or a compatible version -->
            <type>pom</type>
            <scope>import</scope>
        </dependency>
    </dependencies>
</dependencyManagement>
```

✅ 2. Jackson Databind
```
<dependency>
    <groupId>com.fasterxml.jackson.core</groupId>
    <artifactId>jackson-databind</artifactId>
    <version>2.15.3</version> <!-- latest as of now -->
</dependency>
```
# Purpose: JSON (de)serialization – useful for mapping Java objects to/from JSON.

# Latest version is fine unless you're tied to a Spring Boot BOM that restricts it.

✅ 3. AWS Java SDK
```
<dependency>
    <groupId>com.amazonaws</groupId>
    <artifactId>aws-java-sdk</artifactId>
    <version>1.12.775</version>
</dependency>
```
# Purpose: Gives full access to AWS services (like EC2, S3, IAM, etc.)

# Tip: You can reduce bloat by importing only the specific modules you need, e.g., for S3 only:

```
<dependency>
    <groupId>com.amazonaws</groupId>
    <artifactId>aws-java-sdk-s3</artifactId>
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
```
[dev]

aws_access_key_id = YOUR_DEV_ACCESS_KEY

aws_secret_access_key = YOUR_DEV_SECRET_KEY
```

✅ Example of ~/.aws/config file:
```
[default]
region = us-east-1
```

