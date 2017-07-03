## CI/CD Pipeline

### Synopsis

We need a shiny new Continuous Integration/Deployment setup, as what we have currently is not tennable. We are going to build out what we need with Open Source tools as the cost of self-hosting, infrastructure as well as staffing, are lower than the evaluated paid-for black-box cloud solutions, which might inhibit our ability to deliver.

| Team Required  | Est. Project Contribution | Est. Contributors | Components Involved                                      |
|----------------|--------------------------:|:-----------------:|----------------------------------------------------------|
| DevOps         |                       50% |         1         |  CI Pipeline<br/>Configuration Management<br/>Deployment Tooling |
| Infrastructure |                       50% |         2         | Hardware provisioning<br/>Security hardening                 |

### Details

Our current process is extremely slow, and is bottlenecking releases of features. The current state is a disparate system of cobbled together shell scripts and outdated builders that routinely break, and slow us down, forcing us to waste time doing maintanence instead of delivering.

We have evaluated a number of potential solutions, both open and closed source, and free and paid services, and have determined the best course going forward would be to use the following technologies:

- [JenkinsCI](https://jenkins.io/)
- [Docker](https://www.docker.com/)
- [Google Container Engine](https://cloud.google.com/container-engine/)
- [Fabric](http://www.fabfile.org/)

Jenkins will be used to facilitate a pipeline process, that executes the following:

- Clean build of the application
- Test execution
  - Unit tests
  - Integration tests
  - Smoke tests
  - Performance tests
  - Regression tests
- Baking a docker image
- Pushing to GCR for usage in GCE
- Fabric will then execute a Red/Green deploy of the application

### Timelines

The timeline for this project is *ASAP* if possible, but if we do not have the capacity Q4'17 is acceptable.
