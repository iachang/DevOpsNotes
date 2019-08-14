# Here are my personal notes on DevOps!


#### Waterfall Model
* First public documented lifecycle model. 
* Can only progress when the previous stage is complete, and you can never turn back.
**Stages:
1. Requirements - What the project will look like
2. Design - Write code for the application
3. Implement - Building the application (unit testing, debugging, compiling, and packaging)
4. Test - Deploy onto test servers to test
5. Deploy - Deployed onto public release
6. Maintenance - Monitor for any issues with the public release
**Issues:
1. No working software is produced
2. Cannot go back and change something if any new concept or idea is introduced
3. Very risky for any bugs or downtime or any vast changes (like changing the operating system). Requiring looking back at the ENTIRE source code.
4. Very inefficient for large and complex models.

#### Introducing... Agile Methodology!
* Continuous iterations of development and testing throughout the software development life cycle
* The project is broken up into several iterations
* Each iteration is the same time duration (2-8 weeks), and broken up into three parts:
1. Discover: Discover new feature(s) to add
2. Design: Write code for the application
3. Develop: Test, compile, build, and then package the application with the newly added features
* At the end of each iteration, a working and functional product is deployed.
**Stages:
1. Requirements
2. Run the multiple "iterations" as described above to progressively build the entire project in multiple "pieces."
3. Deploy - Once the project is fully complete, deploy the project.
**Issues:
1. Any conflicts or inconsistency in the deployment stage will be a huge inconvenience and one undesriable path must be taken. Takes a long time to fix any buggy upgrade still. For example, the "Dev" team wants change and add more features so the application works on the "Dev" team laptop; but once the application reaches the "Ops" team laptop there is a bug, so the "Ops" team wants stability and fix bugs before deployment. This is because deployment is linear, and not "circular" or "continuous" like the Design, Build, Test phase.
^^ Essentially, the main issue is that the development team is going to be effective because it's continuously developed in small, tiny bite sized increments. However, the operations + development merge is still going to be an extremely large sized merge which will be problematic. We are looking for a solution to cause the dev+ops merge phase to be small and incremental.

What's the solution to both Agile and Waterfall? **DevOps!**

####DevOps
* A methodology that combines the development team (change) and operations team (stability). 
* Studies building constantly evolving and rapidly changing systems at large scale.
* As we labeled above, the Agile **development** methodology involves continuous, "circular" iterations of Discover, Designing, and Developing.
* To continue with DevOps, we need to understand the **operations** methodology. These involve continuous, "circular" iterations of Deploying, Operating, and Monitoring.
* Common technologies matches with each portion: Git/JUnit -> "Dev", Jenkins/Travis CI -> "DevOps (Continuous Integration)", Docker -> "Ops"
* Combining these two, we get something called "Continuous Integration". Allowing merging small code changes and bug fixes in small increments rather than one large change in the end.
* It gets hard to manually test for bugs, so CI services like Travis or Jenkins automates the testing, compiling, building, etc. with automated test scripts once a new feature is developed in the code. This ensures the project is working up and well. Once this build passes, the project is allowed to be deployed.

