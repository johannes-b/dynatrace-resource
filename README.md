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
- name: ufo
  type: dynatrace-resource
  source:
    envid: sampleenvid
    apitoken: sampleapitoken
```

Behavior
--------

### `check`: Nothing yet
### `in`: Nothing yet
### `out`: Nothing yet

#### Parameters

Required:

none

A sample pipeline utilizing this resource can be found in the [PivotalDevOpsPipeline repo.](https://github.com/akirasoft/PivotalDevOpsTutorial)

