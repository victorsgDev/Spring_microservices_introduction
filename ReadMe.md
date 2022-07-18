# Comunicación entre microservicios por medio de OpenFeign
- FeignClient Interfaces: Ejemplo: <br> 

@FeignClient(name = "car-service", url = "http://localhost:8002") <br>
@RequestMapping("/car")<br>
public interface CarFeignClient {

    @PostMapping()
    Car save(@RequestBody Car car);

    @GetMapping("/byuser/{userId}")
    List<Car> getCars(@PathVariable("userId") int userId);
}
- Al llamar a "http://localhost:8001/user/savecar/{userId}" OpenFeign llama a "http://localhost:8002/car/" pero siempre trabajamos con el servicio User (:8001)
