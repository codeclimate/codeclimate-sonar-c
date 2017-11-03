# Code Climate Sonar-C Engine

[![CircleCI](https://circleci.com/gh/codeclimate/codeclimate-sonar-php.svg?style=svg&circle-token=72a9e9a49dc6a8653be6a69321012fe1d84abc3d)](https://circleci.com/gh/codeclimate/codeclimate-sonar-php)
[![Maintainability](https://api.codeclimate.com/v1/badges/2bdcb2e92bbc0efb855b/maintainability)](https://codeclimate.com/github/codeclimate/codeclimate-sonar-php/maintainability)
[![Test Coverage](https://api.codeclimate.com/v1/badges/2bdcb2e92bbc0efb855b/test_coverage)](https://codeclimate.com/github/codeclimate/codeclimate-sonar-php/test_coverage)

`codeclimate-sonar-c` is a Code Climate engine that wraps [Sonarlint](http://www.sonarlint.org) in standalone mode for C/C++ code.

## Installation
```
make image
```

## Tests
```
make test
```

## Plugin
Unlike other plugins, the c-familly is not available from Maven repositories, so the jar has to be manually [downloaded from the project page](https://docs.sonarqube.org/pages/viewpage.action?pageId=7996665)

## Usage

1. If you haven't already, [install the Code Climate CLI](https://github.com/codeclimate/codeclimate).
2. Configure a `.codeclimate.yml` file in your repo.
```yml
engines:
  sonar-c:
    enabled: true
    config:
      tests_patterns:
        - src/test/**
exclude_paths:
  - build/
```
3. Run `codeclimate analyze`.

## Custom configurations

### Severity
Ignore issues with severity below the minimum:
```
engines:
  sonar-c:
    enabled: true
    config:
      minimum_severity: critical  # default: major
                                  # valid values are: info, minor, major, critical, blocker
```

## Sonar Documentation

http://www.sonarlint.org/commandline
http://docs.sonarqube.org/display/SCAN/Analyzing+with+SonarQube+Scanner

Issue Tracker: http://jira.sonarsource.com/browse/SLCLI

## Copyright

See [LICENSE](LICENSE)
