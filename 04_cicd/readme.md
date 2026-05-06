# Домашняя работа к занятию “ CI/CD”
## Рудских Александр

### Скрин успешности выполнения таски в gitlab

Скрин 1:
<img width="1417" height="711" alt="Скрин_1" src="https://github.com/user-attachments/assets/42d511ab-5c62-4273-83d3-248510db4114" />

Скрин 2:
<img width="1192" height="561" alt="Скрин_2" src="https://github.com/user-attachments/assets/f245b8f7-b42b-4a3e-970c-51f8a8dcbbc8" />

**Файл `.gitlab-ci.yml`:**

```yml
---
stages:
  - build
  - test

build-job:
  stage: build
  tags:
    - netology
  script:
    - echo Building
    - mkdir build
    - echo Create_file > build\info.txt
    - type build\info.txt
  artifacts:
    paths:
      - build\info.txt
    expire_in: 1 hour

test-job:
  stage: test
  tags:
    - netology
  script:
    - echo Testing
    - if exist build\info.txt (echo Файл найден && type build\info.txt) else (echo Файл НЕ найден && exit 1)
  dependencies:
    - build-job
