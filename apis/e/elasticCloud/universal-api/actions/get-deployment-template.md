# Elastic Cloud: Get Deployment Template

Retrieves a deployment template from Elastic Cloud.

```
GET https://connect.mindcloud.co/v1/universal/elasticCloud/latest/actions/get-deployment-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Elastic Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/elasticCloud/latest/actions/get-deployment-template?connectionId=$CONNECTION_ID&region=string&templateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "region": "string",
  "templateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/elasticCloud/latest/actions/get-deployment-template?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `region` | string | yes | Region of the deployment template. |
| `showInstanceConfigurations` | boolean | no | Return details for instance configurations referenced by the template. |
| `showMaxZones` | boolean | no | Populate max_zones in the instance configurations response. |
| `stackVersion` | string | no | Adapt the returned template to the specified stack version. |
| `templateId` | string | yes | Identifier for the deployment template. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deploymentTemplate": {
        "resources": {
          "apm": [
            {
              "elasticsearchClusterRefId": "string",
              "plan": {
                "clusterTopology": [
                  {
                    "instanceConfigurationId": "string",
                    "size": {
                      "resource": "string",
                      "value": 1
                    },
                    "zoneCount": 1
                  }
                ]
              },
              "refId": "string",
              "region": "string"
            }
          ],
          "elasticsearch": [
            {
              "plan": {
                "autoscalingEnabled": true,
                "clusterTopology": [
                  {
                    "autoscalingMax": {
                      "resource": "string",
                      "value": 1
                    },
                    "elasticsearch": {
                      "nodeAttributes": {
                        "data": "string"
                      }
                    },
                    "id": "string",
                    "instanceConfigurationId": "string",
                    "nodeRoles": [
                      "string"
                    ],
                    "nodeType": {
                      "data": true,
                      "ingest": true,
                      "master": true
                    },
                    "size": {
                      "resource": "string",
                      "value": 1
                    },
                    "topologyElementControl": {
                      "min": {
                        "resource": "string",
                        "value": 1
                      }
                    },
                    "zoneCount": 1
                  }
                ]
              },
              "refId": "string",
              "region": "string",
              "settings": {
                "dedicatedMastersThreshold": 1
              }
            }
          ],
          "enterpriseSearch": [
            {
              "elasticsearchClusterRefId": "string",
              "plan": {
                "clusterTopology": [
                  {
                    "instanceConfigurationId": "string",
                    "nodeType": {
                      "appserver": true,
                      "connector": true,
                      "worker": true
                    },
                    "size": {
                      "resource": "string",
                      "value": 1
                    },
                    "zoneCount": 1
                  }
                ]
              },
              "refId": "string",
              "region": "string"
            }
          ],
          "integrationsServer": [
            {
              "elasticsearchClusterRefId": "string",
              "plan": {
                "clusterTopology": [
                  {
                    "instanceConfigurationId": "string",
                    "size": {
                      "resource": "string",
                      "value": 1
                    },
                    "zoneCount": 1
                  }
                ]
              },
              "refId": "string",
              "region": "string"
            }
          ],
          "kibana": [
            {
              "elasticsearchClusterRefId": "string",
              "plan": {
                "clusterTopology": [
                  {
                    "instanceConfigurationId": "string",
                    "size": {
                      "resource": "string",
                      "value": 1
                    },
                    "zoneCount": 1
                  }
                ]
              },
              "refId": "string",
              "region": "string"
            }
          ]
        },
        "settings": {
          "autoscalingEnabled": true
        }
      },
      "description": "string",
      "id": "string",
      "instanceConfigurations": [
        {
          "configVersion": 1,
          "cpuMultiplier": 1,
          "description": "string",
          "discreteSizes": {
            "defaultSize": 1,
            "resource": "string",
            "sizes": [
              1
            ]
          },
          "id": "string",
          "instanceType": "string",
          "metadata": {
            "sku": "string"
          },
          "name": "Ava Chen",
          "nodeTypes": [
            "string"
          ],
          "storageMultiplier": 1
        }
      ],
      "metadata": [
        {
          "key": "string",
          "value": "string"
        }
      ],
      "name": "Ava Chen",
      "order": 1,
      "systemOwned": true,
      "templateCategoryId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deploymentTemplate.resources.apm[].elasticsearchClusterRefId` | string |  |
| `deploymentTemplate.resources.apm[].plan.clusterTopology[].instanceConfigurationId` | string |  |
| `deploymentTemplate.resources.apm[].plan.clusterTopology[].size.resource` | string |  |
| `deploymentTemplate.resources.apm[].plan.clusterTopology[].size.value` | number |  |
| `deploymentTemplate.resources.apm[].plan.clusterTopology[].zoneCount` | number |  |
| `deploymentTemplate.resources.apm[].refId` | string |  |
| `deploymentTemplate.resources.apm[].region` | string |  |
| `deploymentTemplate.resources.elasticsearch[].plan.autoscalingEnabled` | boolean |  |
| `deploymentTemplate.resources.elasticsearch[].plan.clusterTopology[].autoscalingMax.resource` | string |  |
| `deploymentTemplate.resources.elasticsearch[].plan.clusterTopology[].autoscalingMax.value` | number |  |
| `deploymentTemplate.resources.elasticsearch[].plan.clusterTopology[].elasticsearch.nodeAttributes.data` | string |  |
| `deploymentTemplate.resources.elasticsearch[].plan.clusterTopology[].id` | string |  |
| `deploymentTemplate.resources.elasticsearch[].plan.clusterTopology[].instanceConfigurationId` | string |  |
| `deploymentTemplate.resources.elasticsearch[].plan.clusterTopology[].nodeRoles[]` | string |  |
| `deploymentTemplate.resources.elasticsearch[].plan.clusterTopology[].nodeType.data` | boolean |  |
| `deploymentTemplate.resources.elasticsearch[].plan.clusterTopology[].nodeType.ingest` | boolean |  |
| `deploymentTemplate.resources.elasticsearch[].plan.clusterTopology[].nodeType.master` | boolean |  |
| `deploymentTemplate.resources.elasticsearch[].plan.clusterTopology[].size.resource` | string |  |
| `deploymentTemplate.resources.elasticsearch[].plan.clusterTopology[].size.value` | number |  |
| `deploymentTemplate.resources.elasticsearch[].plan.clusterTopology[].topologyElementControl.min.resource` | string |  |
| `deploymentTemplate.resources.elasticsearch[].plan.clusterTopology[].topologyElementControl.min.value` | number |  |
| `deploymentTemplate.resources.elasticsearch[].plan.clusterTopology[].zoneCount` | number |  |
| `deploymentTemplate.resources.elasticsearch[].refId` | string |  |
| `deploymentTemplate.resources.elasticsearch[].region` | string |  |
| `deploymentTemplate.resources.elasticsearch[].settings.dedicatedMastersThreshold` | number |  |
| `deploymentTemplate.resources.enterpriseSearch[].elasticsearchClusterRefId` | string |  |
| `deploymentTemplate.resources.enterpriseSearch[].plan.clusterTopology[].instanceConfigurationId` | string |  |
| `deploymentTemplate.resources.enterpriseSearch[].plan.clusterTopology[].nodeType.appserver` | boolean |  |
| `deploymentTemplate.resources.enterpriseSearch[].plan.clusterTopology[].nodeType.connector` | boolean |  |
| `deploymentTemplate.resources.enterpriseSearch[].plan.clusterTopology[].nodeType.worker` | boolean |  |
| `deploymentTemplate.resources.enterpriseSearch[].plan.clusterTopology[].size.resource` | string |  |
| `deploymentTemplate.resources.enterpriseSearch[].plan.clusterTopology[].size.value` | number |  |
| `deploymentTemplate.resources.enterpriseSearch[].plan.clusterTopology[].zoneCount` | number |  |
| `deploymentTemplate.resources.enterpriseSearch[].refId` | string |  |
| `deploymentTemplate.resources.enterpriseSearch[].region` | string |  |
| `deploymentTemplate.resources.integrationsServer[].elasticsearchClusterRefId` | string |  |
| `deploymentTemplate.resources.integrationsServer[].plan.clusterTopology[].instanceConfigurationId` | string |  |
| `deploymentTemplate.resources.integrationsServer[].plan.clusterTopology[].size.resource` | string |  |
| `deploymentTemplate.resources.integrationsServer[].plan.clusterTopology[].size.value` | number |  |
| `deploymentTemplate.resources.integrationsServer[].plan.clusterTopology[].zoneCount` | number |  |
| `deploymentTemplate.resources.integrationsServer[].refId` | string |  |
| `deploymentTemplate.resources.integrationsServer[].region` | string |  |
| `deploymentTemplate.resources.kibana[].elasticsearchClusterRefId` | string |  |
| `deploymentTemplate.resources.kibana[].plan.clusterTopology[].instanceConfigurationId` | string |  |
| `deploymentTemplate.resources.kibana[].plan.clusterTopology[].size.resource` | string |  |
| `deploymentTemplate.resources.kibana[].plan.clusterTopology[].size.value` | number |  |
| `deploymentTemplate.resources.kibana[].plan.clusterTopology[].zoneCount` | number |  |
| `deploymentTemplate.resources.kibana[].refId` | string |  |
| `deploymentTemplate.resources.kibana[].region` | string |  |
| `deploymentTemplate.settings.autoscalingEnabled` | boolean |  |
| `description` | string |  |
| `id` | string |  |
| `instanceConfigurations[].configVersion` | number |  |
| `instanceConfigurations[].cpuMultiplier` | number |  |
| `instanceConfigurations[].description` | string |  |
| `instanceConfigurations[].discreteSizes.defaultSize` | number |  |
| `instanceConfigurations[].discreteSizes.resource` | string |  |
| `instanceConfigurations[].discreteSizes.sizes[]` | number |  |
| `instanceConfigurations[].id` | string |  |
| `instanceConfigurations[].instanceType` | string |  |
| `instanceConfigurations[].metadata.sku` | string |  |
| `instanceConfigurations[].name` | string |  |
| `instanceConfigurations[].nodeTypes[]` | string |  |
| `instanceConfigurations[].storageMultiplier` | number |  |
| `metadata[].key` | string |  |
| `metadata[].value` | string |  |
| `name` | string |  |
| `order` | number |  |
| `systemOwned` | boolean |  |
| `templateCategoryId` | string |  |

## Native endpoint

Through the native Elastic Cloud API, this operation is `GET /deployments/templates/:template_id` (base URL `https://api.elastic-cloud.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-deployment-template.md) for the provider-specific parameters and requirements.

