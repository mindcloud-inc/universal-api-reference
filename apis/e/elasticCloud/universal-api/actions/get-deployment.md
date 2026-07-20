# Elastic Cloud: Get Deployment

Retrieves a deployment from Elastic Cloud.

```
GET https://connect.mindcloud.co/v1/universal/elasticCloud/latest/actions/get-deployment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Elastic Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/elasticCloud/latest/actions/get-deployment?connectionId=$CONNECTION_ID&deploymentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "deploymentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/elasticCloud/latest/actions/get-deployment?${params}`, {
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
| `clearTransient` | boolean | no | Remove transient sections from child resources in the response. |
| `convertLegacyPlans` | boolean | no | Convert legacy plans to the 2.x format in the response. |
| `deploymentId` | string | yes | Identifier for the deployment. |
| `enrichWithTemplate` | boolean | no | Enrich plan data with missing elements from the deployment template. |
| `forceAllPlanHistory` | boolean | no | Return the full plan history even when it is very large. |
| `showInstanceConfigurations` | boolean | no | Return details for each instance configuration referenced by the deployment. |
| `showInstanceMetrics` | boolean | no | Include resource instance metrics in the response. |
| `showMetadata` | boolean | no | Include full cluster metadata in the response. |
| `showPlanDefaults` | boolean | no | Show values that remain at their default values in the plan response. |
| `showPlanHistory` | boolean | no | Include plan history with current and pending plan information. |
| `showPlanLogs` | boolean | no | Include attempt logs with current and pending plan information. |
| `showPlans` | boolean | no | Include current and pending plan information in the response. |
| `showSecurity` | boolean | no | Include Elasticsearch security information in the response. |
| `showSettings` | boolean | no | Include cluster settings in the response. |
| `showSystemAlerts` | number | no | Number of system alerts to include in the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "healthy": true,
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
      "metadata": {
        "byokEnabled": true,
        "createdAt": "string",
        "hidden": true,
        "lastModified": "string",
        "lastResourcePlanModified": "string",
        "organizationId": "string",
        "ownerId": "string",
        "systemOwned": true
      },
      "name": "Ava Chen",
      "resources": {
        "elasticsearch": [
          {
            "id": "string",
            "info": {
              "associatedApmClusters": [
                {
                  "apmId": "string",
                  "enabled": true
                }
              ],
              "associatedKibanaClusters": [
                {
                  "enabled": true,
                  "kibanaId": "string"
                }
              ],
              "clusterId": "string",
              "clusterName": "Ava Chen",
              "deploymentId": "string",
              "elasticsearch": {
                "blockingIssues": {
                  "healthy": true
                },
                "clusterBlockingIssues": {
                  "healthy": true
                },
                "healthy": true,
                "masterInfo": {
                  "healthy": true,
                  "masters": [
                    {
                      "instances": [
                        "string"
                      ],
                      "masterInstanceName": "Ava Chen",
                      "masterNodeId": "string"
                    }
                  ]
                },
                "shardInfo": {
                  "healthy": true
                },
                "shardsStatus": {
                  "status": "string"
                }
              },
              "healthy": true,
              "locked": true,
              "metadata": {
                "ccr": true,
                "cloudId": "string",
                "endpoint": "string",
                "lastModified": "string",
                "ports": {
                  "http": 1,
                  "https": 1,
                  "transportPassthrough": 1
                },
                "serviceUrl": "https://example.com",
                "ssoDeepLinkingSupported": true,
                "version": 1
              },
              "planInfo": {
                "current": {
                  "attemptEndTime": "string",
                  "attemptStartTime": "string",
                  "healthy": true,
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
                        "instanceConfigurationVersion": 1,
                        "nodeRoles": [
                          "string"
                        ],
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
                    ],
                    "deploymentTemplate": {
                      "id": "string"
                    },
                    "elasticsearch": {
                      "version": "string"
                    }
                  },
                  "planAttemptId": "string",
                  "source": {
                    "action": "string",
                    "date": "string",
                    "facilitator": "string"
                  }
                },
                "healthy": true
              },
              "region": "string",
              "snapshots": {
                "count": 1,
                "healthy": true,
                "latestEndTime": "string",
                "latestStatus": "string",
                "latestSuccessful": true,
                "latestSuccessfulEndTime": "string",
                "recentSuccess": true,
                "scheduledTime": "string"
              },
              "status": "string",
              "topology": {
                "healthy": true,
                "instances": [
                  {
                    "allocatorId": "string",
                    "containerStarted": true,
                    "disk": {
                      "diskSpaceAvailable": 1,
                      "diskSpaceUsed": 1,
                      "storageMultiplier": 1
                    },
                    "healthy": true,
                    "instanceConfiguration": {
                      "configVersion": 1,
                      "id": "string",
                      "name": "Ava Chen",
                      "resource": "string"
                    },
                    "instanceName": "Ava Chen",
                    "instanceSetId": "string",
                    "logicalZone": "string",
                    "maintenanceMode": true,
                    "memory": {
                      "instanceCapacity": 1,
                      "memoryPressure": 1,
                      "nativeMemoryPressure": 1
                    },
                    "nodeRoles": [
                      "string"
                    ],
                    "serviceRoles": [
                      "string"
                    ],
                    "serviceRunning": true,
                    "serviceVersion": "string",
                    "zone": "string"
                  }
                ]
              }
            },
            "refId": "string",
            "region": "string"
          }
        ],
        "integrationsServer": [
          {
            "elasticsearchClusterRefId": "string",
            "id": "string",
            "info": {
              "apmServerMode": "string",
              "deploymentId": "string",
              "elasticsearchCluster": {
                "elasticsearchId": "string"
              },
              "healthy": true,
              "id": "string",
              "metadata": {
                "ccr": true,
                "endpoint": "string",
                "lastModified": "string",
                "ports": {
                  "http": 1,
                  "https": 1,
                  "transportPassthrough": 1
                },
                "servicesUrls": [
                  {
                    "service": "https://example.com",
                    "url": "https://example.com"
                  }
                ],
                "serviceUrl": "https://example.com",
                "ssoDeepLinkingSupported": true,
                "version": 1
              },
              "name": "Ava Chen",
              "planInfo": {
                "current": {
                  "attemptEndTime": "string",
                  "attemptStartTime": "string",
                  "healthy": true,
                  "plan": {
                    "autoscalingEnabled": true,
                    "clusterTopology": [
                      {
                        "instanceConfigurationId": "string",
                        "instanceConfigurationVersion": 1,
                        "size": {
                          "resource": "string",
                          "value": 1
                        },
                        "zoneCount": 1
                      }
                    ],
                    "integrationsServer": {
                      "systemSettings": {
                        "secretToken": "string"
                      },
                      "version": "string"
                    }
                  },
                  "planAttemptId": "string",
                  "source": {
                    "action": "string",
                    "date": "string",
                    "facilitator": "string"
                  }
                },
                "healthy": true
              },
              "region": "string",
              "status": "string",
              "topology": {
                "healthy": true,
                "instances": [
                  {
                    "allocatorId": "string",
                    "containerStarted": true,
                    "healthy": true,
                    "instanceConfiguration": {
                      "configVersion": 1,
                      "id": "string",
                      "name": "Ava Chen",
                      "resource": "string"
                    },
                    "instanceName": "Ava Chen",
                    "logicalZone": "string",
                    "maintenanceMode": true,
                    "memory": {
                      "instanceCapacity": 1,
                      "nativeMemoryPressure": 1
                    },
                    "serviceRunning": true,
                    "serviceVersion": "string",
                    "zone": "string"
                  }
                ]
              }
            },
            "refId": "string",
            "region": "string"
          }
        ],
        "kibana": [
          {
            "elasticsearchClusterRefId": "string",
            "id": "string",
            "info": {
              "clusterId": "string",
              "clusterName": "Ava Chen",
              "deploymentId": "string",
              "elasticsearchCluster": {
                "elasticsearchId": "string"
              },
              "healthy": true,
              "metadata": {
                "ccr": true,
                "endpoint": "string",
                "lastModified": "string",
                "ports": {
                  "http": 1,
                  "https": 1,
                  "transportPassthrough": 1
                },
                "servicesUrls": [
                  {
                    "service": "https://example.com",
                    "url": "https://example.com"
                  }
                ],
                "serviceUrl": "https://example.com",
                "ssoDeepLinkingSupported": true,
                "ssoEntityId": "string",
                "ssoUrl": "https://example.com",
                "version": 1
              },
              "planInfo": {
                "current": {
                  "attemptEndTime": "string",
                  "attemptStartTime": "string",
                  "healthy": true,
                  "plan": {
                    "autoscalingEnabled": true,
                    "clusterTopology": [
                      {
                        "instanceConfigurationId": "string",
                        "instanceConfigurationVersion": 1,
                        "size": {
                          "resource": "string",
                          "value": 1
                        },
                        "zoneCount": 1
                      }
                    ],
                    "kibana": {
                      "version": "string"
                    }
                  },
                  "planAttemptId": "string",
                  "source": {
                    "action": "string",
                    "date": "string",
                    "facilitator": "string"
                  }
                },
                "healthy": true
              },
              "region": "string",
              "status": "string",
              "topology": {
                "healthy": true,
                "instances": [
                  {
                    "allocatorId": "string",
                    "containerStarted": true,
                    "healthy": true,
                    "instanceConfiguration": {
                      "configVersion": 1,
                      "id": "string",
                      "name": "Ava Chen",
                      "resource": "string"
                    },
                    "instanceName": "Ava Chen",
                    "logicalZone": "string",
                    "maintenanceMode": true,
                    "memory": {
                      "instanceCapacity": 1,
                      "nativeMemoryPressure": 1
                    },
                    "serviceRunning": true,
                    "serviceVersion": "string",
                    "zone": "string"
                  }
                ]
              }
            },
            "refId": "string",
            "region": "string"
          }
        ]
      },
      "settings": {
        "autoOps": {
          "status": "string"
        },
        "autoscalingEnabled": true,
        "solutionType": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `healthy` | boolean |  |
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
| `metadata.byokEnabled` | boolean |  |
| `metadata.createdAt` | string |  |
| `metadata.hidden` | boolean |  |
| `metadata.lastModified` | string |  |
| `metadata.lastResourcePlanModified` | string |  |
| `metadata.organizationId` | string |  |
| `metadata.ownerId` | string |  |
| `metadata.systemOwned` | boolean |  |
| `name` | string |  |
| `resources.elasticsearch[].id` | string |  |
| `resources.elasticsearch[].info.associatedApmClusters[].apmId` | string |  |
| `resources.elasticsearch[].info.associatedApmClusters[].enabled` | boolean |  |
| `resources.elasticsearch[].info.associatedKibanaClusters[].enabled` | boolean |  |
| `resources.elasticsearch[].info.associatedKibanaClusters[].kibanaId` | string |  |
| `resources.elasticsearch[].info.clusterId` | string |  |
| `resources.elasticsearch[].info.clusterName` | string |  |
| `resources.elasticsearch[].info.deploymentId` | string |  |
| `resources.elasticsearch[].info.elasticsearch.blockingIssues.healthy` | boolean |  |
| `resources.elasticsearch[].info.elasticsearch.clusterBlockingIssues.healthy` | boolean |  |
| `resources.elasticsearch[].info.elasticsearch.healthy` | boolean |  |
| `resources.elasticsearch[].info.elasticsearch.masterInfo.healthy` | boolean |  |
| `resources.elasticsearch[].info.elasticsearch.masterInfo.masters[].instances[]` | string |  |
| `resources.elasticsearch[].info.elasticsearch.masterInfo.masters[].masterInstanceName` | string |  |
| `resources.elasticsearch[].info.elasticsearch.masterInfo.masters[].masterNodeId` | string |  |
| `resources.elasticsearch[].info.elasticsearch.shardInfo.healthy` | boolean |  |
| `resources.elasticsearch[].info.elasticsearch.shardsStatus.status` | string |  |
| `resources.elasticsearch[].info.healthy` | boolean |  |
| `resources.elasticsearch[].info.locked` | boolean |  |
| `resources.elasticsearch[].info.metadata.ccr` | boolean |  |
| `resources.elasticsearch[].info.metadata.cloudId` | string |  |
| `resources.elasticsearch[].info.metadata.endpoint` | string |  |
| `resources.elasticsearch[].info.metadata.lastModified` | string |  |
| `resources.elasticsearch[].info.metadata.ports.http` | number |  |
| `resources.elasticsearch[].info.metadata.ports.https` | number |  |
| `resources.elasticsearch[].info.metadata.ports.transportPassthrough` | number |  |
| `resources.elasticsearch[].info.metadata.serviceUrl` | string |  |
| `resources.elasticsearch[].info.metadata.ssoDeepLinkingSupported` | boolean |  |
| `resources.elasticsearch[].info.metadata.version` | number |  |
| `resources.elasticsearch[].info.planInfo.current.attemptEndTime` | string |  |
| `resources.elasticsearch[].info.planInfo.current.attemptStartTime` | string |  |
| `resources.elasticsearch[].info.planInfo.current.healthy` | boolean |  |
| `resources.elasticsearch[].info.planInfo.current.plan.autoscalingEnabled` | boolean |  |
| `resources.elasticsearch[].info.planInfo.current.plan.clusterTopology[].autoscalingMax.resource` | string |  |
| `resources.elasticsearch[].info.planInfo.current.plan.clusterTopology[].autoscalingMax.value` | number |  |
| `resources.elasticsearch[].info.planInfo.current.plan.clusterTopology[].elasticsearch.nodeAttributes.data` | string |  |
| `resources.elasticsearch[].info.planInfo.current.plan.clusterTopology[].id` | string |  |
| `resources.elasticsearch[].info.planInfo.current.plan.clusterTopology[].instanceConfigurationId` | string |  |
| `resources.elasticsearch[].info.planInfo.current.plan.clusterTopology[].instanceConfigurationVersion` | number |  |
| `resources.elasticsearch[].info.planInfo.current.plan.clusterTopology[].nodeRoles[]` | string |  |
| `resources.elasticsearch[].info.planInfo.current.plan.clusterTopology[].size.resource` | string |  |
| `resources.elasticsearch[].info.planInfo.current.plan.clusterTopology[].size.value` | number |  |
| `resources.elasticsearch[].info.planInfo.current.plan.clusterTopology[].topologyElementControl.min.resource` | string |  |
| `resources.elasticsearch[].info.planInfo.current.plan.clusterTopology[].topologyElementControl.min.value` | number |  |
| `resources.elasticsearch[].info.planInfo.current.plan.clusterTopology[].zoneCount` | number |  |
| `resources.elasticsearch[].info.planInfo.current.plan.deploymentTemplate.id` | string |  |
| `resources.elasticsearch[].info.planInfo.current.plan.elasticsearch.version` | string |  |
| `resources.elasticsearch[].info.planInfo.current.planAttemptId` | string |  |
| `resources.elasticsearch[].info.planInfo.current.source.action` | string |  |
| `resources.elasticsearch[].info.planInfo.current.source.date` | string |  |
| `resources.elasticsearch[].info.planInfo.current.source.facilitator` | string |  |
| `resources.elasticsearch[].info.planInfo.healthy` | boolean |  |
| `resources.elasticsearch[].info.region` | string |  |
| `resources.elasticsearch[].info.snapshots.count` | number |  |
| `resources.elasticsearch[].info.snapshots.healthy` | boolean |  |
| `resources.elasticsearch[].info.snapshots.latestEndTime` | string |  |
| `resources.elasticsearch[].info.snapshots.latestStatus` | string |  |
| `resources.elasticsearch[].info.snapshots.latestSuccessful` | boolean |  |
| `resources.elasticsearch[].info.snapshots.latestSuccessfulEndTime` | string |  |
| `resources.elasticsearch[].info.snapshots.recentSuccess` | boolean |  |
| `resources.elasticsearch[].info.snapshots.scheduledTime` | string |  |
| `resources.elasticsearch[].info.status` | string |  |
| `resources.elasticsearch[].info.topology.healthy` | boolean |  |
| `resources.elasticsearch[].info.topology.instances[].allocatorId` | string |  |
| `resources.elasticsearch[].info.topology.instances[].containerStarted` | boolean |  |
| `resources.elasticsearch[].info.topology.instances[].disk.diskSpaceAvailable` | number |  |
| `resources.elasticsearch[].info.topology.instances[].disk.diskSpaceUsed` | number |  |
| `resources.elasticsearch[].info.topology.instances[].disk.storageMultiplier` | number |  |
| `resources.elasticsearch[].info.topology.instances[].healthy` | boolean |  |
| `resources.elasticsearch[].info.topology.instances[].instanceConfiguration.configVersion` | number |  |
| `resources.elasticsearch[].info.topology.instances[].instanceConfiguration.id` | string |  |
| `resources.elasticsearch[].info.topology.instances[].instanceConfiguration.name` | string |  |
| `resources.elasticsearch[].info.topology.instances[].instanceConfiguration.resource` | string |  |
| `resources.elasticsearch[].info.topology.instances[].instanceName` | string |  |
| `resources.elasticsearch[].info.topology.instances[].instanceSetId` | string |  |
| `resources.elasticsearch[].info.topology.instances[].logicalZone` | string |  |
| `resources.elasticsearch[].info.topology.instances[].maintenanceMode` | boolean |  |
| `resources.elasticsearch[].info.topology.instances[].memory.instanceCapacity` | number |  |
| `resources.elasticsearch[].info.topology.instances[].memory.memoryPressure` | number |  |
| `resources.elasticsearch[].info.topology.instances[].memory.nativeMemoryPressure` | number |  |
| `resources.elasticsearch[].info.topology.instances[].nodeRoles[]` | string |  |
| `resources.elasticsearch[].info.topology.instances[].serviceRoles[]` | string |  |
| `resources.elasticsearch[].info.topology.instances[].serviceRunning` | boolean |  |
| `resources.elasticsearch[].info.topology.instances[].serviceVersion` | string |  |
| `resources.elasticsearch[].info.topology.instances[].zone` | string |  |
| `resources.elasticsearch[].refId` | string |  |
| `resources.elasticsearch[].region` | string |  |
| `resources.integrationsServer[].elasticsearchClusterRefId` | string |  |
| `resources.integrationsServer[].id` | string |  |
| `resources.integrationsServer[].info.apmServerMode` | string |  |
| `resources.integrationsServer[].info.deploymentId` | string |  |
| `resources.integrationsServer[].info.elasticsearchCluster.elasticsearchId` | string |  |
| `resources.integrationsServer[].info.healthy` | boolean |  |
| `resources.integrationsServer[].info.id` | string |  |
| `resources.integrationsServer[].info.metadata.ccr` | boolean |  |
| `resources.integrationsServer[].info.metadata.endpoint` | string |  |
| `resources.integrationsServer[].info.metadata.lastModified` | string |  |
| `resources.integrationsServer[].info.metadata.ports.http` | number |  |
| `resources.integrationsServer[].info.metadata.ports.https` | number |  |
| `resources.integrationsServer[].info.metadata.ports.transportPassthrough` | number |  |
| `resources.integrationsServer[].info.metadata.servicesUrls[].service` | string |  |
| `resources.integrationsServer[].info.metadata.servicesUrls[].url` | string |  |
| `resources.integrationsServer[].info.metadata.serviceUrl` | string |  |
| `resources.integrationsServer[].info.metadata.ssoDeepLinkingSupported` | boolean |  |
| `resources.integrationsServer[].info.metadata.version` | number |  |
| `resources.integrationsServer[].info.name` | string |  |
| `resources.integrationsServer[].info.planInfo.current.attemptEndTime` | string |  |
| `resources.integrationsServer[].info.planInfo.current.attemptStartTime` | string |  |
| `resources.integrationsServer[].info.planInfo.current.healthy` | boolean |  |
| `resources.integrationsServer[].info.planInfo.current.plan.autoscalingEnabled` | boolean |  |
| `resources.integrationsServer[].info.planInfo.current.plan.clusterTopology[].instanceConfigurationId` | string |  |
| `resources.integrationsServer[].info.planInfo.current.plan.clusterTopology[].instanceConfigurationVersion` | number |  |
| `resources.integrationsServer[].info.planInfo.current.plan.clusterTopology[].size.resource` | string |  |
| `resources.integrationsServer[].info.planInfo.current.plan.clusterTopology[].size.value` | number |  |
| `resources.integrationsServer[].info.planInfo.current.plan.clusterTopology[].zoneCount` | number |  |
| `resources.integrationsServer[].info.planInfo.current.plan.integrationsServer.systemSettings.secretToken` | string |  |
| `resources.integrationsServer[].info.planInfo.current.plan.integrationsServer.version` | string |  |
| `resources.integrationsServer[].info.planInfo.current.planAttemptId` | string |  |
| `resources.integrationsServer[].info.planInfo.current.source.action` | string |  |
| `resources.integrationsServer[].info.planInfo.current.source.date` | string |  |
| `resources.integrationsServer[].info.planInfo.current.source.facilitator` | string |  |
| `resources.integrationsServer[].info.planInfo.healthy` | boolean |  |
| `resources.integrationsServer[].info.region` | string |  |
| `resources.integrationsServer[].info.status` | string |  |
| `resources.integrationsServer[].info.topology.healthy` | boolean |  |
| `resources.integrationsServer[].info.topology.instances[].allocatorId` | string |  |
| `resources.integrationsServer[].info.topology.instances[].containerStarted` | boolean |  |
| `resources.integrationsServer[].info.topology.instances[].healthy` | boolean |  |
| `resources.integrationsServer[].info.topology.instances[].instanceConfiguration.configVersion` | number |  |
| `resources.integrationsServer[].info.topology.instances[].instanceConfiguration.id` | string |  |
| `resources.integrationsServer[].info.topology.instances[].instanceConfiguration.name` | string |  |
| `resources.integrationsServer[].info.topology.instances[].instanceConfiguration.resource` | string |  |
| `resources.integrationsServer[].info.topology.instances[].instanceName` | string |  |
| `resources.integrationsServer[].info.topology.instances[].logicalZone` | string |  |
| `resources.integrationsServer[].info.topology.instances[].maintenanceMode` | boolean |  |
| `resources.integrationsServer[].info.topology.instances[].memory.instanceCapacity` | number |  |
| `resources.integrationsServer[].info.topology.instances[].memory.nativeMemoryPressure` | number |  |
| `resources.integrationsServer[].info.topology.instances[].serviceRunning` | boolean |  |
| `resources.integrationsServer[].info.topology.instances[].serviceVersion` | string |  |
| `resources.integrationsServer[].info.topology.instances[].zone` | string |  |
| `resources.integrationsServer[].refId` | string |  |
| `resources.integrationsServer[].region` | string |  |
| `resources.kibana[].elasticsearchClusterRefId` | string |  |
| `resources.kibana[].id` | string |  |
| `resources.kibana[].info.clusterId` | string |  |
| `resources.kibana[].info.clusterName` | string |  |
| `resources.kibana[].info.deploymentId` | string |  |
| `resources.kibana[].info.elasticsearchCluster.elasticsearchId` | string |  |
| `resources.kibana[].info.healthy` | boolean |  |
| `resources.kibana[].info.metadata.ccr` | boolean |  |
| `resources.kibana[].info.metadata.endpoint` | string |  |
| `resources.kibana[].info.metadata.lastModified` | string |  |
| `resources.kibana[].info.metadata.ports.http` | number |  |
| `resources.kibana[].info.metadata.ports.https` | number |  |
| `resources.kibana[].info.metadata.ports.transportPassthrough` | number |  |
| `resources.kibana[].info.metadata.servicesUrls[].service` | string |  |
| `resources.kibana[].info.metadata.servicesUrls[].url` | string |  |
| `resources.kibana[].info.metadata.serviceUrl` | string |  |
| `resources.kibana[].info.metadata.ssoDeepLinkingSupported` | boolean |  |
| `resources.kibana[].info.metadata.ssoEntityId` | string |  |
| `resources.kibana[].info.metadata.ssoUrl` | string |  |
| `resources.kibana[].info.metadata.version` | number |  |
| `resources.kibana[].info.planInfo.current.attemptEndTime` | string |  |
| `resources.kibana[].info.planInfo.current.attemptStartTime` | string |  |
| `resources.kibana[].info.planInfo.current.healthy` | boolean |  |
| `resources.kibana[].info.planInfo.current.plan.autoscalingEnabled` | boolean |  |
| `resources.kibana[].info.planInfo.current.plan.clusterTopology[].instanceConfigurationId` | string |  |
| `resources.kibana[].info.planInfo.current.plan.clusterTopology[].instanceConfigurationVersion` | number |  |
| `resources.kibana[].info.planInfo.current.plan.clusterTopology[].size.resource` | string |  |
| `resources.kibana[].info.planInfo.current.plan.clusterTopology[].size.value` | number |  |
| `resources.kibana[].info.planInfo.current.plan.clusterTopology[].zoneCount` | number |  |
| `resources.kibana[].info.planInfo.current.plan.kibana.version` | string |  |
| `resources.kibana[].info.planInfo.current.planAttemptId` | string |  |
| `resources.kibana[].info.planInfo.current.source.action` | string |  |
| `resources.kibana[].info.planInfo.current.source.date` | string |  |
| `resources.kibana[].info.planInfo.current.source.facilitator` | string |  |
| `resources.kibana[].info.planInfo.healthy` | boolean |  |
| `resources.kibana[].info.region` | string |  |
| `resources.kibana[].info.status` | string |  |
| `resources.kibana[].info.topology.healthy` | boolean |  |
| `resources.kibana[].info.topology.instances[].allocatorId` | string |  |
| `resources.kibana[].info.topology.instances[].containerStarted` | boolean |  |
| `resources.kibana[].info.topology.instances[].healthy` | boolean |  |
| `resources.kibana[].info.topology.instances[].instanceConfiguration.configVersion` | number |  |
| `resources.kibana[].info.topology.instances[].instanceConfiguration.id` | string |  |
| `resources.kibana[].info.topology.instances[].instanceConfiguration.name` | string |  |
| `resources.kibana[].info.topology.instances[].instanceConfiguration.resource` | string |  |
| `resources.kibana[].info.topology.instances[].instanceName` | string |  |
| `resources.kibana[].info.topology.instances[].logicalZone` | string |  |
| `resources.kibana[].info.topology.instances[].maintenanceMode` | boolean |  |
| `resources.kibana[].info.topology.instances[].memory.instanceCapacity` | number |  |
| `resources.kibana[].info.topology.instances[].memory.nativeMemoryPressure` | number |  |
| `resources.kibana[].info.topology.instances[].serviceRunning` | boolean |  |
| `resources.kibana[].info.topology.instances[].serviceVersion` | string |  |
| `resources.kibana[].info.topology.instances[].zone` | string |  |
| `resources.kibana[].refId` | string |  |
| `resources.kibana[].region` | string |  |
| `settings.autoOps.status` | string |  |
| `settings.autoscalingEnabled` | boolean |  |
| `settings.solutionType` | string |  |

## Native endpoint

Through the native Elastic Cloud API, this operation is `GET /deployments/:deployment_id` (base URL `https://api.elastic-cloud.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-deployment.md) for the provider-specific parameters and requirements.

