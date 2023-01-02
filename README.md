## Introduction:

Thanks to [Gary Clarke's Tutorials](https://www.youtube.com/@GaryClarkeTech), I have prepared this repository containing the following images as services in a docker container:

1. php-fpm 8.1
2. nginx the latest version
3. mysql 8.0
4. phpmyadmin the latest version   
   And after installation you will also have:   
   composer 2.5  
   symfony cli 5.4  
   
Use this repository to start your development. Just create your symfony project inside the app directory like:  
```
- symfony new . --version=5.4
```
## installation:
1. Clone the repository
2. Go to the directory of the repository and make copy of the ".env.example" and save it with ".env" name.
3. Run:
```
 - docker compose -f docker-compose.dev.yaml up --build -d
```  
4. **Do not forget to change git origin to point your project**:
```
- git remote rm origin
- git remote add origin <your repository url>
```  
Make a great stuff!