Dynatrace UFO resource for Concourse
====================================

Allows pushing deployment event data to Dynatrace
Allows pulling performance metrics from Dynatrace to validate builds
Used within the [PivotalDevOpsPipeline demo](https://github.com/akirasoft/PivotalDevOpsTutorial)

Resource Type Configuration
---------------------------

```yaml
resource_types:
- name: dynatrace-resource
  type: docker-image
  source:
    repository: mvilliger/dynatrace-resource
```

Source Configuration
--------------------

```yaml
- name: dynatrace
  type: dynatrace-resource
  source:
    apitoken: sampleapitoken
    tenanthost: sampletenanthost
```

Behavior
--------

### `check`: Nothing yet
### `in`: Nothing yet

### `out`: Pushes Deployment event to Dynatrace

Pushes a deployment event to Dynatrace to the service specified in the monspec file

#### Parameters

Required:
- `APP_REPO`: Must match name of resource containing monspec file
- `monspecserviceenvironment`: Must match toplevel entry in monspec file plus environment name, i.e. "SampleJSonService/Staging"
- `pipelinetaskname`: Label for the task/job being executed, i.e.: "TestStagingDeployment"
- `deployversion`: a version number for the release, i.e.: "v1.4"

A sample pipeline utilizing this resource can be found in the [PivotalDevOpsPipeline repo.](https://github.com/akirasoft/PivotalDevOpsTutorial)

