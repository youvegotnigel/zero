# Zero

Zero is our feature rich, core test automation framework, that can be used as an underlying automation framework
for any/and all kind of test automation frameworks (such as API, Browser, Mobile App).

![build status](https://img.shields.io/github/actions/workflow/status/pramodkumaryadav/zero/trigger-tests-on-pull-request.yml?logo=GitHub)
![open issues](https://img.shields.io/github/issues/PramodKumarYadav/zero)
![forks](https://img.shields.io/github/forks/PramodKumarYadav/zero)
![stars](https://img.shields.io/github/stars/PramodKumarYadav/zero)
![license](https://img.shields.io/github/license/PramodKumarYadav/zero?style=flat-square)
![languages](https://img.shields.io/github/languages/count/pramodkumaryadav/zero)

![info](https://img.shields.io/static/v1?label=with-love&message=from-power-tester&color=blue?style=plastic&logo=appveyor)

### Requiring (one time) manual setup by user

1. [JDK 11](https://www.oracle.com/java/technologies/javase/jdk11-archive-downloads.html) - as language of choice for writing this test framework.
2. [Maven 3.8.6+](https://maven.apache.org/) - for project dependency management and running tests in CI. 
3. [git-crypt](https://dev.to/heroku/how-to-manage-your-secrets-with-git-crypt-56ih) - to encrypt/decrypt secrets. [One time set up instructions here](docs/README-GIT-CRYPT.md).


## Working principles

- [ ] **Problem solving based learning** (Learn something when a problem comes. This way, you will remember it better).
- [ ] **First make it work, then make it better** (Specially when working with new tools or tech, don't worry about getting it right the first time. First focus on making it work, then refactor to make it better)  

## Test goals and objectives

A good guideline to test any project is:

>> Test the right things, in the right order, at the right time.

- [ ] **Risk based testing** (Test the right things and avoid testing 3rd party/low risk software).  
- [ ] **Follow test pyramid** (in the right order)
- [ ] **Fail fast, fail early** (at the right time)  
- [ ] **Prevent breaking changes from merging** (Run fast and stable API tests as a part of application pull requests).
- [ ] **If cannot prevent, test immediately on merge** Run slower and flaky Mobile/Browser tests immediately on merge of pull requests on new deployed env.
- [ ] **Test asap, if cannot test on merge** Use your creative imagination to do exploratory tests, UX testing post merge.  

## Test framework goals and objectives

Some of the key goals and objectives of our test framework are:  

- [ ] **Easy to understand** (Separate test intentions from implementation)  
- [ ] **Easy to maintain** (Separation of concerns between data, config, code and tests).
- [ ] **Easy to scale** (Prefer composition over inheritance. Follow SOLID principles).
- [ ] **Fast execution time** (Create atomic, independent tests that can run in parallel to cut down on execution times).
- [ ] **Test at right moment** (Have various CI workflows that allow testing as soon as possible).
- [ ] **Reliable, robust tests** (Create generic classes that have methods that wait for the right state before acting on elements)  
- [ ] **Flexible tests that can run on any test env** (Move all env related information to its own config files, so that tests can flexibly run on any test environment)

## Important files

There are some standard files, there deserves a section of their own. These are:

- [x] **README.md file** (This is where you tell what your project is all about and how others can use it.).
- [x] **junit-platform.properties file** (This is where you specify your projects execution mode i.e. serial, or any of the available parallel execution modes)  
- [x] **.log4j properties file**. (This specifies the log level for your project)
- [x] **application.conf and other conf file**. (This is where we specify common application config and config for each test environment)
- [x] **.gitignore file**. (This contains everything that you are *not* interested in version controlling.)  
- [ ] **.gitattributes file**. (This is where you specify attributes of any files that are being version controlled.)
- [ ] **.editorconfig file**. (This provides a way to have a common formatting rules within your team. In absence of this, your PRs would be a mess to review.)  
- [x] **pom.xml file**. (This is where you define all your maven project dependencies.)  
- [x] **LICENSE file**. (This is where you give permission to others to make use of your open source project.)
- [ ] **Dockerfile**. (This is where you automate your test environment. i.e. all the parts that your project depends on; such as having a machine, JDK, Maven, setting up system environments, any other tools, etc all.)
- [ ] **.dockerignore file**. (Like gitignore file, here we specify everything that we want to be ignored from passing to docker build context.)
- [ ] **docker-compose.yml file**. (A convenient way to set up a local instance of your dockerized application on your localhost machine. )  

## Tool Set

Key tools to be used in this core framework are:

- [x] **Java** (As the core programming language)
- [x] **Maven** (for automatic dependency management)
- [x] **Junit 5** (for assertions)
- [x] **Slf4J/Log4J** (for logging interface and as a logging library)
- [x] **Typesafe** (for application configuration for multiple test environments)
- [x] **Git crypt** (for managing secrets)
- [ ] **Surefire** (for xml reports in CI)
- [ ] **Surefire Site plugin** (for html reports in CI)  
- [x] **Github** (for version control)
- [x] **Github actions** (for continuous integration)
- [ ] **Faker library** (for generating random test data for different locales - germany, france, netherlands, english)  
- [x] **Slack integration** (for giving notifications on pull requests)
- [ ] **Elastic and Kibana** (for test monitoring)
- [ ] **Docker** (for automating test framework's environment)
- [ ] **Powershell or bash Script** (for automating building test environment)
- [ ] **SonarQube/SonarLint** (for keeping your code clean and safe)
- [x] **Badges** (for a quick view on your project meta and build status)

Key tools that we will use in other frameworks, that will all extend this core framework are:

- [ ] **RestAssured**  (library for Rest API automation)
- [ ] **Selenium**  (library for Browser automation)
- [ ] **Appium**  (library for Mobile ios/android automation)

## end to end test automation process

![end-to-end-test-process](./images/end-to-end-test-workflow.png)

## References

- [README-wiki](https://en.wikipedia.org/wiki/README)
- [how-to-write-a-good-readme-file](https://www.freecodecamp.org/news/how-to-write-a-good-readme-file/)
- [another-good-readme-example](https://github.com/othneildrew/Best-README-Template)
- [java-gitignore-file-example](https://gist.github.com/dedunumax/54e82214715e35439227)
- [manage multiple github accounts](https://www.freecodecamp.org/news/manage-multiple-github-accounts-the-ssh-way-2dadc30ccaca/)
- [manage multiple git configs for different accounts](https://www.freecodecamp.org/news/how-to-handle-multiple-git-configurations-in-one-machine/)
- [logout/login in multiple accounts](https://medium.com/@devesu/how-to-logout-from-git-in-windows-e17c66fe9ca8)
- [adding ssh key to the ssh agent](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)
- [adding-a-new-ssh-key-to-your-github-account](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account)
- [auto launching ssh keys for git on windows](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/working-with-ssh-key-passphrases#auto-launching-ssh-agent-on-git-for-windows)
- [GitCredentialManager](https://github.com/GitCredentialManager)
