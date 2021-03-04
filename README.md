# Spring Boot Single Sign-on Example Application

### Build and run SSO SERVER

Run maven script:

```bash
cd sso-server
mvn clean compile
mvn spring-boot:run
```

Build success:
```bash
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  5.784 s
[INFO] Finished at: 2021-03-03T21:48:02-05:00
[INFO] ------------------------------------------------------------------------
```

Server app run success:
```bash
2021-03-03 22:05:50.354  INFO 86852 --- [           main] o.s.c.support.DefaultLifecycleProcessor  : Starting beans in phase 0
2021-03-03 22:05:50.430  INFO 86852 --- [           main] s.b.c.e.t.TomcatEmbeddedServletContainer : Tomcat started on port(s): 8080 (http)
2021-03-03 22:05:50.433  INFO 86852 --- [           main] c.m.ssoserver.SsoServerApplication       : Started SsoServerApplication in 2.752 seconds (JVM running for 5.029)
```

### Build and run CLIENT

Run maven script:

```bash
cd client
mvn clean compile
mvn spring-boot:run
```

Build success:
```bash
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  5.521 s
[INFO] Finished at: 2021-03-03T22:01:40-05:00
[INFO] ------------------------------------------------------------------------
```

Client app run success:
```bash
2021-03-03 22:03:03.723  INFO 86473 --- [           main] o.s.c.support.DefaultLifecycleProcessor  : Starting beans in phase 0
2021-03-03 22:03:03.804  INFO 86473 --- [           main] s.b.c.e.t.TomcatEmbeddedServletContainer : Tomcat started on port(s): 8082 (http)
2021-03-03 22:03:03.808  INFO 86473 --- [           main] c.maratgaliev.client.ClientApplication   : Started ClientApplication in 3.428 seconds (JVM running for 5.874)
```

### Testing

- Run http://localhost:8080/sso-server
- Run http://localhost:8082/client (you will be redirected)
- Login with: user/password
- You should be redirected to the http://localhost:8082/client with welcome message

