The purpose of this Quick Start is to show you how easily and quickly you can get a simple API up and running using swagger-node.

* [Get an API up and running](#upandrunning)
* [Open the Swagger editor](#openeditor)

### <a name="upandrunning"></a>Get an API up and running

First, we create a new swagger-node project and test the default "hello world"API.

1. Install swagger-node, as described in the [installation guide](install.md).

2. Create swagger-node project directory and cd to it. This is where you'll create your first project. 

3. Execute the project create command: 

    `swagger project create hello-world`

4. Pick the API framework you want to use. We're going to pick express:
    ```
    ? Framework? (Use arrow keys)
      connect
    ❯ express
      hapi
      restify
      sails
    ```
5. swagger-node clones a skeleton project from GitHub that's pre-configured to use the Express framework. It then runs `npm install` to pick up the dependencies. 

>Note: Windows users see the [note below](#windows-note) regarding npm. 

6. Change to the new project directory: `cd hello-world`

7. Type `swagger project start` to start your API.  You now have an API running with swagger-node!

8. In another terminal, run this command: 

    `curl http://127.0.0.1:10010/hello?name=Scott`  

    And, you'll get back the response `Hello, Scott`.

That's it - You have now created, started and tested your first API project with swagger-node! 

### <a name="openeditor"></a>Open the Swagger editor

The Swagger editor lets you design and test your API interactively. While you design and test, the API documentation is generated automatically for you. 

Now that we've got our basic API running, let's open the Swagger editor.

1. Be sure you're in your project root directory: `./hello-world`. 
 
2. Fire up the editor: `swagger project edit`

*The Swagger editor*
![alt text](./images/swagger-editor.png)


### <a name='windows-note'></a>Windows Users
For some versions of npm on Windows will have problems on the `npm install` step of `swagger project create`.  They are related to a `debug` module on npm not being managed properly.  The following steps should resolve this issue:

1. In the project directory, execute the following commands:
  1. `npm install yamljs`
  2. `npm install debug`
  3. `npm install swagger-tools`

Now, when you run `swagger project start` your project should start successfully.