version: 2.1

workflows:
  test-env-vars:
    jobs:
      - build

jobs:
  build:
    docker:
      - image: cimg/base:2020.01
    steps:
      - checkout
      - run:
          name: "echo an env var that is part of our project"
          command: |
            echo $MY_ENV_VAR# cicdvariables
training


