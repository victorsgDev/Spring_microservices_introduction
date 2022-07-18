# Comunicación entre microservicios por medio de RestTemplate
* RestTemplate Bean
* Car & bike models
* UserController : getCars & getBikes
* UserService : List<Car> cars = restTemplate.getForObject("http://localhost:8002/car/byuser/" + userId, List.class);
  List<Bike> bikes = restTemplate.getForObject("http://localhost:8003/bike/byuser/" + userId, List.class);