# swagger-java-client

PAAS平台docker-yard管理系统
- API version: 1.0
  - Build date: 2019-04-09T11:58:57.392Z

更多信息请联系基础框架团队


*Automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen)*


## Requirements

Building the API client library requires:
1. Java 1.7+
2. Maven/Gradle

## Installation

To install the API client library to your local Maven repository, simply execute:

```shell
mvn clean install
```

To deploy it to a remote Maven repository instead, configure the settings of the repository and execute:

```shell
mvn clean deploy
```

Refer to the [OSSRH Guide](http://central.sonatype.org/pages/ossrh-guide.html) for more information.

### Maven users

Add this dependency to your project's POM:

```xml
<dependency>
  <groupId>io.swagger</groupId>
  <artifactId>swagger-java-client</artifactId>
  <version>1.0.0</version>
  <scope>compile</scope>
</dependency>
```

### Gradle users

Add this dependency to your project's build file:

```groovy
compile "io.swagger:swagger-java-client:1.0.0"
```

### Others

At first generate the JAR by executing:

```shell
mvn clean package
```

Then manually install the following JARs:

* `target/swagger-java-client-1.0.0.jar`
* `target/lib/*.jar`

## Getting Started

Please follow the [installation](#installation) instruction and execute the following Java code:

```java

import com.ppdai.dockeryard.client.*;
import com.ppdai.dockeryard.client.auth.*;
import com.ppdai.dockeryard.client.model.*;
import com.ppdai.dockeryard.client.api.ImageControllerApi;

import java.io.File;
import java.util.*;

public class ImageControllerApiExample {

    public static void main(String[] args) {
        
        ImageControllerApi apiInstance = new ImageControllerApi();
        Long id = 789L; // Long | id
        try {
            String result = apiInstance.deleteImageUsingDELETE(id);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling ImageControllerApi#deleteImageUsingDELETE");
            e.printStackTrace();
        }
    }
}

```

## Documentation for API Endpoints

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*ImageControllerApi* | [**deleteImageUsingDELETE**](docs/ImageControllerApi.md#deleteImageUsingDELETE) | **DELETE** /api/image/{id} | 删除image
*ImageControllerApi* | [**getAllImagesUsingGET**](docs/ImageControllerApi.md#getAllImagesUsingGET) | **GET** /api/image/all | 获取所有image列表
*ImageControllerApi* | [**getImageByAppNameUsingGET**](docs/ImageControllerApi.md#getImageByAppNameUsingGET) | **GET** /api/image/app | 根据appName获取image列表
*ImageControllerApi* | [**getImageUsingGET**](docs/ImageControllerApi.md#getImageUsingGET) | **GET** /api/image/{id} | 根据id获取image
*ImageControllerApi* | [**getImagesByParamUsingGET**](docs/ImageControllerApi.md#getImagesByParamUsingGET) | **GET** /api/images | 根据获取image列表


## Documentation for Models

 - [ImageEntity](docs/ImageEntity.md)
 - [ImagePageVO](docs/ImagePageVO.md)


## Documentation for Authorization

All endpoints do not require authorization.
Authentication schemes defined for the API:

## Recommendation

It's recommended to create an instance of `ApiClient` per thread in a multithreaded environment to avoid any potential issues.

## Author


