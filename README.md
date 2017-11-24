# Getting started

A sample API that uses a petstore as an example to demonstrate features in the OpenAPI 3.0 specification

## How to Build

This client library is a Ruby gem which can be compiled and used in your Ruby and Ruby on Rails project. This library requires a few gems from the RubyGems repository.

1. Open the command line interface or the terminal and navigate to the folder containing the source code.
2. Run ``` gem build swagger_petstore.gemspec ``` to build the gem.
3. Once built, the gem can be installed on the current work environment using ``` gem install swagger_petstore-1.0.0.gem ```

![Building Gem](https://apidocs.io/illustration/ruby?step=buildSDK&workspaceFolder=Swagger%20Petstore-Ruby&workspaceName=Swagger%20Petstore-Ruby&projectName=swagger_petstore&gemName=swagger_petstore&gemVer=1.0.0)

## How to Use

The following section explains how to use the SwaggerPetstore Ruby Gem in a new Rails project using RubyMine&trade;. The basic workflow presented here is also applicable if you prefer using a different editor or IDE.

### 1. Starting a new project

Close any existing projects in RubyMine&trade; by selecting ``` File -> Close Project ```. Next, click on ``` Create New Project ``` to create a new project from scratch.

![Create a new project in RubyMine](https://apidocs.io/illustration/ruby?step=createNewProject0&workspaceFolder=Swagger%20Petstore-Ruby&workspaceName=SwaggerPetstore&projectName=swagger_petstore&gemName=swagger_petstore&gemVer=1.0.0)

Next, provide ``` TestApp ``` as the project name, choose ``` Rails Application ``` as the project type, and click ``` OK ```.

![Create a new Rails Application in RubyMine - step 1](https://apidocs.io/illustration/ruby?step=createNewProject1&workspaceFolder=Swagger%20Petstore-Ruby&workspaceName=SwaggerPetstore&projectName=swagger_petstore&gemName=swagger_petstore&gemVer=1.0.0)

In the next dialog make sure that correct *Ruby SDK* is being used (minimum 2.0.0) and click ``` OK ```.

![Create a new Rails Application in RubyMine - step 2](https://apidocs.io/illustration/ruby?step=createNewProject2&workspaceFolder=Swagger%20Petstore-Ruby&workspaceName=SwaggerPetstore&projectName=swagger_petstore&gemName=swagger_petstore&gemVer=1.0.0)

This will create a new Rails Application project with an existing set of files and folder.

### 2. Add reference of the gem

In order to use the SwaggerPetstore gem in the new project we must add a gem reference. Locate the ```Gemfile``` in the *Project Explorer* window under the ``` TestApp ``` project node. The file contains references to all gems being used in the project. Here, add the reference to the library gem by adding the following line: ``` gem 'swagger_petstore', '~> 1.0.0' ```

![Add references of the Gemfile](https://apidocs.io/illustration/ruby?step=addReference&workspaceFolder=Swagger%20Petstore-Ruby&workspaceName=SwaggerPetstore&projectName=swagger_petstore&gemName=swagger_petstore&gemVer=1.0.0)

### 3. Adding a new Rails Controller

Once the ``` TestApp ``` project is created, a folder named ``` controllers ``` will be visible in the *Project Explorer* under the following path: ``` TestApp > app > controllers ```. Right click on this folder and select ``` New -> Run Rails Generator... ```.

![Run Rails Generator on Controllers Folder](https://apidocs.io/illustration/ruby?step=addCode0&workspaceFolder=Swagger%20Petstore-Ruby&workspaceName=SwaggerPetstore&projectName=swagger_petstore&gemName=swagger_petstore&gemVer=1.0.0)

Selecting the said option will popup a small window where the generator names are displayed. Here, select the ``` controller ``` template.

![Create a new Controller](https://apidocs.io/illustration/ruby?step=addCode1&workspaceFolder=Swagger%20Petstore-Ruby&workspaceName=SwaggerPetstore&projectName=swagger_petstore&gemName=swagger_petstore&gemVer=1.0.0)

Next, a popup window will ask you for a Controller name and included Actions. For controller name provide ``` Hello ``` and include an action named ``` Index ``` and click ``` OK ```.

![Add a new Controller](https://apidocs.io/illustration/ruby?step=addCode2&workspaceFolder=Swagger%20Petstore-Ruby&workspaceName=SwaggerPetstore&projectName=swagger_petstore&gemName=swagger_petstore&gemVer=1.0.0)

A new controller class anmed ``` HelloController ``` will be created in a file named ``` hello_controller.rb ``` containing a method named ``` Index ```. In this method, add code for initialization and a sample for its usage.

![Initialize the library](https://apidocs.io/illustration/ruby?step=addCode3&workspaceFolder=Swagger%20Petstore-Ruby&workspaceName=SwaggerPetstore&projectName=swagger_petstore&gemName=swagger_petstore&gemVer=1.0.0)

## How to Test

You can test the generated SDK and the server with automatically generated test
cases as follows:

  1. From terminal/cmd navigate to the root directory of the SDK.
  2. Invoke: `bundle exec rake`

## Initialization

### 

API client can be initialized as following.

```ruby

client = SwaggerPetstore::SwaggerPetstoreClient.new
```

The added initlization code can be debugged by putting a breakpoint in the ``` Index ``` method and running the project in debug mode by selecting ``` Run -> Debug 'Development: TestApp' ```.

![Debug the TestApp](https://apidocs.io/illustration/ruby?step=addCode4&workspaceFolder=Swagger%20Petstore-Ruby&workspaceName=SwaggerPetstore&projectName=swagger_petstore&gemName=swagger_petstore&gemVer=1.0.0&initLine=client%2520%253D%2520SwaggerPetstoreClient.new)



# Class Reference

## <a name="list_of_controllers"></a>List of Controllers

* [APIController](#api_controller)

## <a name="api_controller"></a>![Class: ](https://apidocs.io/img/class.png ".APIController") APIController

### Get singleton instance

The singleton instance of the ``` APIController ``` class can be accessed from the API Client.

```ruby
client = client.client
```

### <a name="add_pet"></a>![Method: ](https://apidocs.io/img/method.png ".APIController.add_pet") add_pet

> *Tags:*  ``` Skips Authentication ``` 

> Creates a new pet in the store.  Duplicates are allowed


```ruby
def add_pet(body); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | Pet to add to the store |


#### Example Usage

```ruby
body = NewPet.new

result = client.add_pet(body)

```

#### Errors

| Error Code | Error Description |
|------------|-------------------|
| 0 | unexpected error |



### <a name="delete_pet"></a>![Method: ](https://apidocs.io/img/method.png ".APIController.delete_pet") delete_pet

> *Tags:*  ``` Skips Authentication ``` 

> deletes a single pet based on the ID supplied


```ruby
def delete_pet(id); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | ID of pet to delete |


#### Example Usage

```ruby
id = 192

client.delete_pet(id)

```

#### Errors

| Error Code | Error Description |
|------------|-------------------|
| 0 | unexpected error |



### <a name="find_pets"></a>![Method: ](https://apidocs.io/img/method.png ".APIController.find_pets") find_pets

> *Tags:*  ``` Skips Authentication ``` 

> Returns all pets from the system that the user has access to
> Nam sed condimentum est. Maecenas tempor sagittis sapien, nec rhoncus sem sagittis sit amet. Aenean at gravida augue, ac iaculis sem. Curabitur odio lorem, ornare eget elementum nec, cursus id lectus. Duis mi turpis, pulvinar ac eros ac, tincidunt varius justo. In hac habitasse platea dictumst. Integer at adipiscing ante, a sagittis ligula. Aenean pharetra tempor ante molestie imperdiet. Vivamus id aliquam diam. Cras quis velit non tortor eleifend sagittis. Praesent at enim pharetra urna volutpat venenatis eget eget mauris. In eleifend fermentum facilisis. Praesent enim enim, gravida ac sodales sed, placerat id erat. Suspendisse lacus dolor, consectetur non augue vel, vehicula interdum libero. Morbi euismod sagittis libero sed lacinia.
> 
> Sed tempus felis lobortis leo pulvinar rutrum. Nam mattis velit nisl, eu condimentum ligula luctus nec. Phasellus semper velit eget aliquet faucibus. In a mattis elit. Phasellus vel urna viverra, condimentum lorem id, rhoncus nibh. Ut pellentesque posuere elementum. Sed a varius odio. Morbi rhoncus ligula libero, vel eleifend nunc tristique vitae. Fusce et sem dui. Aenean nec scelerisque tortor. Fusce malesuada accumsan magna vel tempus. Quisque mollis felis eu dolor tristique, sit amet auctor felis gravida. Sed libero lorem, molestie sed nisl in, accumsan tempor nisi. Fusce sollicitudin massa ut lacinia mattis. Sed vel eleifend lorem. Pellentesque vitae felis pretium, pulvinar elit eu, euismod sapien.
> 


```ruby
def find_pets(tags = nil,
                  limit = nil); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| tags |  ``` Optional ```  ``` Collection ```  | tags to filter by |
| limit |  ``` Optional ```  | maximum number of results to return |


#### Example Usage

```ruby
tags = ['tags']
limit = 192

result = client.find_pets(tags, limit)

```

#### Errors

| Error Code | Error Description |
|------------|-------------------|
| 0 | unexpected error |



### <a name="find_pet_by_id"></a>![Method: ](https://apidocs.io/img/method.png ".APIController.find_pet_by_id") find_pet_by_id

> *Tags:*  ``` Skips Authentication ``` 

> Returns a user based on a single ID, if the user does not have access to the pet


```ruby
def find_pet_by_id(id); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | ID of pet to fetch |


#### Example Usage

```ruby
id = 192

result = client.find_pet_by_id(id)

```

#### Errors

| Error Code | Error Description |
|------------|-------------------|
| 0 | unexpected error |



[Back to List of Controllers](#list_of_controllers)



