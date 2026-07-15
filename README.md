# Fixtures
Fixture repositories used for testing

Accessible at: https://content-services.github.io/fixtures/

## Local Testing

To serve all fixtures locally, run a Python HTTP server from the `fixtures/` directory:

```bash
cd fixtures && python3 -m http.server 8989
```

Fixtures are then accessible at `http://localhost:8989/`, for example:
- `http://localhost:8989/yum/comps-modules/v1/`
- `http://localhost:8989/maven/com/example/fixture/fixture-package-a/1.0.0.rhlw-00001/com.example.fixture.fixture-package-a.1.0.0.rhlw-00001.pom`

## Contributing

Avoid modifying existing fixtures unless you are sure it is necessary or safe to do so
