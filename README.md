# 09-ci-03-cicd

## Подготовка к выполнению

### Виртуальные машины:
![VM](./pictures/VM.png)

### Nexus:
![Nexus](./pictures/Nexus.png)

### SonarQube:
![SonarQube](./pictures/SonarQube.png)

## Знакомоство с SonarQube

### Основная часть

``` bash
sonar-scanner --version
```
![SonarVersion](./pictures/Sonar-scanner-version.png)

Тест кода ./example/fail.py:

``` bash
sonar-scanner -Dsonar.projectKey=tvm2360-example -Dsonar.sources=. -Dsonar.host.url=http://51.250.114.130:9000 -Dsonar.login=4a9151ce170ea3e57a704dd95a7161ae76d109ae -Dsonar.coverage.exclusions=fail.py
```

![SonarTestShell1](./pictures/Sonar_shell_test1_1.png)

![SonarTestShell2](./pictures/Sonar_shell_test1_2.png)

![SonarTestShell3](./pictures/Sonar_shell_test1_3.png)

Результат:

![SonarTest1Result](./pictures/Sonar_web_test1.png)

Bugs:

![SonarTest1ResultBugs](./pictures/Sonar_web_test1_bugs.png)

Code Smells:

![SonarTest1ResultCodeSmells](./pictures/Sonar_web_test1_code_smells.png)

Результат повторного теста после исправления:

![SonarTest2Result](./pictures/Sonar_web_test2.png)

