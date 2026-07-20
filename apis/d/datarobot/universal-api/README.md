# <img src="https://images.mindcloud.co/apps/icons/datarobotcom_1775842144234.png" alt="Datarobot logo" width="28" height="28"> Datarobot: Universal API

DataRobot is an enterprise AI platform for building, deploying, and managing machine learning and generative AI workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/datarobot/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 32
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.datarobot.com/
- **Vendor API docs:** https://docs.datarobot.com/en/docs/api/reference/index.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Deployments](actions/list-deployments.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/list-deployments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (32)

### Cases

| Action | Method | Description |
| --- | --- | --- |
| [Get Use Case](actions/get-use-case.md) | GET | Retrieves details for a use case from Datarobot. |
| [List Use Cases](actions/list-use-cases.md) | GET | Retrieves a list of use cases from Datarobot. |

### Datasets

| Action | Method | Description |
| --- | --- | --- |
| [Get Dataset](actions/get-dataset.md) | GET | Retrieves details for a dataset from Datarobot. |
| [Get Dataset Version](actions/get-dataset-version.md) | GET | Retrieves details for a dataset version from Datarobot. |
| [Get Use Case Dataset](actions/get-use-case-dataset.md) | GET | Retrieves dataset details for a use case from Datarobot. |
| [List Dataset Versions](actions/list-dataset-versions.md) | GET | Retrieves versions for a dataset from Datarobot. |
| [List Datasets](actions/list-datasets.md) | GET | Retrieves a list of datasets from Datarobot. |
| [List Use Case Datasets](actions/list-use-case-datasets.md) | GET | Retrieves datasets for a use case from Datarobot. |

### Deployments

| Action | Method | Description |
| --- | --- | --- |
| [Get Deployment](actions/get-deployment.md) | GET | Retrieves details for a deployment from Datarobot. |
| [Get Deployment Agent Card](actions/get-deployment-agent-card.md) | GET | Retrieves the agent card for a deployment from Datarobot. |
| [List Deployment Capabilities](actions/list-deployment-capabilities.md) | GET | Retrieves capabilities for a deployment from Datarobot. |
| [List Deployment Challengers](actions/list-deployment-challengers.md) | GET | Retrieves challenger models for a deployment from Datarobot. |
| [List Deployment Custom Metrics](actions/list-deployment-custom-metrics.md) | GET | Retrieves custom metrics for a deployment from Datarobot. |
| [List Deployments](actions/list-deployments.md) | GET | Retrieves a list of deployments from Datarobot. |
| [List Registered Model Deployments](actions/list-registered-model-deployments.md) | GET | Retrieves deployments for a registered model from Datarobot. |
| [List Registered Model Version Deployments](actions/list-registered-model-version-deployments.md) | GET | Retrieves deployments for a registered model version from Datarobot. |
| [List Use Case Deployments](actions/list-use-case-deployments.md) | GET | Retrieves deployments for a use case from Datarobot. |

### Models

| Action | Method | Description |
| --- | --- | --- |
| [Get Custom Model](actions/get-custom-model.md) | GET | Retrieves details for a custom model from Datarobot. |
| [Get Custom Model Version](actions/get-custom-model-version.md) | GET | Retrieves details for a custom model version from Datarobot. |
| [Get Registered Model](actions/get-registered-model.md) | GET | Retrieves details for a registered model from Datarobot. |
| [Get Registered Model Version](actions/get-registered-model-version.md) | GET | Retrieves details for a registered model version from Datarobot. |
| [List Custom Model Versions](actions/list-custom-model-versions.md) | GET | Retrieves versions for a custom model from Datarobot. |
| [List Custom Models](actions/list-custom-models.md) | GET | Retrieves a list of custom models from Datarobot. |
| [List Project Models](actions/list-project-models.md) | GET | Retrieves models for a project from Datarobot. |
| [List Registered Model Versions](actions/list-registered-model-versions.md) | GET | Retrieves versions for a registered model from Datarobot. |
| [List Registered Models](actions/list-registered-models.md) | GET | Retrieves a list of registered models from Datarobot. |
| [List Use Case Registered Models](actions/list-use-case-registered-models.md) | GET | Retrieves registered models for a use case from Datarobot. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET | Retrieves details for a project from Datarobot. |
| [Get Project Status](actions/get-project-status.md) | GET | Retrieves the status of a project from Datarobot. |
| [List Dataset Projects](actions/list-dataset-projects.md) | GET | Retrieves projects for a dataset from Datarobot. |
| [List Projects](actions/list-projects.md) | GET | Retrieves a list of projects from Datarobot. |
| [List Use Case Projects](actions/list-use-case-projects.md) | GET | Retrieves projects for a use case from Datarobot. |

