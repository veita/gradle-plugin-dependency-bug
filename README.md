
## Requirements

The tests requires an NVD API key be set through the `nvdApiKey` property.

https://nvd.nist.gov/developers/request-an-api-key


## Reproduce the problem

```bash
git clone https://github.com/veita/gradle-plugin-dependency-bug.git
cd gradle-plugin-dependency-bug
```

Reproduce the NoSuchFieldError: READ_DATE_TIMESTAMPS_AS_NANOSECONDS

```bash
./gradlew dependencyCheckAnalyze --stacktrace
```

Show how `jackson-databind:2.14.1` is pulled in.

```bash
./gradlew buildEnvironment dependencyCheckAnalyze
```
