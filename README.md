## Introduction:

Thanks to [Gary Clarke's Tutorials](https://www.youtube.com/@GaryClarkeTech), I have prepared this repository containing the following images as services in a docker container:

1. php-fpm 8.1
2. nginx the latest version
3. mysql 8.0
4. phpmyadmin the latest version   
   And after installation you will also have:   
   composer 2.5  
   symfony cli 5.4  
   
Use this repository to start your development. Just do the following steps in order.

## installation:
1. Clone the repository
   . you can change directory's name of the project as yours with this command:
   ````
   - git clone https://github.com/shaho1090/docker-symfonycli.git ./my_project_name
   ````
2. Then change directory:
   ````
   - cd my_project_name
   ````
3. Make copy of the **.env.example** file with name **.env** :   
   ````
   - copy .env.example .env
   ````
4. Make **app** directory
   ````
   - mkdir app
   ````
5. Run:  
   ```
   - docker compose -f docker-compose.dev.yaml up --build -d
   ```
6. Change directory:   
   ````
   - cd app
   ````
7. Install your new symfony project:  
   ````
   - symfony new . --version=5.4 --no-git
   ````
   Wait for installation to complete, then:  
      
8. **Do not forget to change git origin to point your project's repository in root directory**:
    ````
    - cd ..
    - git remote rm origin
    - git remote add origin <your repository url>
    - git push -u origin main
    ````      
   Also consider the ports in the dev environment:
      ```
      app: localhost:8100
      mysql: 4800
      phpmyadmin: localhost:8088
      ```
**_Make a great stuff!_**
