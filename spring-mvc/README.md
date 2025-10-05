# Spring MVC 정리



Model, View, Controller 구조를 기반으로 코드의 관심사 분리

* **Model** : 데이터 저장소, 비즈니스 로직 ( Entity, DTO, Service )
* **View** : 사용자에게 보여지는 화면(Thymeleaf, Mustache, REST API 를 통한 JSON 응답)
* **Controller** : 입력/요청 처리(@Controller, @RestController)

=>  각각의 역할이 명확하게 분리되어 유지보수성과 확장성 우수



###### DispatcherServlet

* 사용자가 요청한 URL 을 통해 요청을 처리할 컨트롤러 결정, 처리된 결과 반환
* 모든 요청을 한 곳에서 관리하는 Front Controller



###### 요청 흐름

Client -> DispatcherServlet -> HandlerMapping -> Controller -> Service/Repository -> Model -> ViewResolver -> View 렌더링 -> Client



###### 어노테이션

* @Controller : 해당 클래스를 컨트롤러로 지정
* @GetMapping : 특정 GET 요청을 이 메서드와 매핑
* @RequestMapping : 다양한 HTTP 메서드(GET, POST, PUT, DELETE.. )에 따른 요청 처리 설정
