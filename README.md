# swivl-test-api

1. installation:
- `git clone swivl_test_api`
- `cd swivl_test_api`
- `composer install`
- `mysql -u root`
- `CREATE DATABASE swivl_test_api`;
- `exit`
- `php bin/console doctrine:migrations:migrate`

2. start server:
- `php -S localhost:8000 -t public`

3. test:
- create class room: 
  `curl -X POST "http://localhost:8000/api/class_rooms" -H "accept: application/json" -H "Content-Type: application/json" -d "{ \"name\": \"test2\",\"createdAt\":\"2019-04-04\", \"isActive\": true}"`
- get class rooms list:
  `curl -X GET "http://localhost:8000/api/class_rooms" -H "accept: application/json"`
- get one class room:
  `curl -X GET "http://localhost:8000/api/class_rooms/1" -H "accept: application/json"`
- update class (set is active / is not active):
  `curl -X PUT "http://localhost:8000/api/class_rooms/1" -H "accept: application/json" -H "Content-Type: application/json" -d "{ \"isActive\": false}"`
- delete class room:
  `curl -X DELETE "http://localhost:8000/api/class_rooms/1" -H "accept: application/json"`
  
