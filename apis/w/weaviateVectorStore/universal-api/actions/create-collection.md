# Weaviate Vector Store: Create Collection

Creates a new collection in Weaviate.

```
POST https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/create-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Weaviate Vector Store `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/create-collection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "class": "string",
  "properties[0].dataType[0]": "text",
  "properties[0].name": "Ava Chen",
  "vectorizer": "none"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/create-collection', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "class": "string",
    "properties[0].dataType[0]": "text",
    "properties[0].name": "Ava Chen",
    "vectorizer": "none"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `class` | string | yes | The collection class name to create. |
| `multiTenancyConfig.enabled` | boolean | no | Whether multi-tenancy is enabled. Default: `false`. |
| `properties[0].dataType[0]` | string | yes | The first property data type. Default: `text`. |
| `properties[0].name` | string | yes | The first property name to create. |
| `vectorizer` | string | yes | The vectorizer for the collection. Default: `none`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "class": "string",
      "invertedIndexConfig": {
        "bm25": {
          "b": 1,
          "k1": 1
        },
        "cleanupIntervalSeconds": 1,
        "stopwords": {
          "preset": "string"
        },
        "usingBlockMaxWAND": true
      },
      "multiTenancyConfig": {
        "autoTenantActivation": true,
        "autoTenantCreation": true,
        "enabled": true
      },
      "properties": [
        {
          "dataType": [
            [
              "string"
            ]
          ],
          "indexFilterable": true,
          "indexRangeFilters": true,
          "indexSearchable": true,
          "name": "Ava Chen",
          "tokenization": "string"
        }
      ],
      "replicationConfig": {
        "asyncEnabled": true,
        "deletionStrategy": "string",
        "factor": 1
      },
      "shardingConfig": {
        "actualCount": 1,
        "actualVirtualCount": 1,
        "desiredCount": 1,
        "desiredVirtualCount": 1,
        "function": "string",
        "key": "string",
        "strategy": "string",
        "virtualPerPhysical": 1
      },
      "vectorIndexConfig": {
        "bq": {
          "enabled": true
        },
        "cleanupIntervalSeconds": 1,
        "distance": "string",
        "dynamicEfFactor": 1,
        "dynamicEfMax": 1,
        "dynamicEfMin": 1,
        "ef": 1,
        "efConstruction": 1,
        "filterStrategy": "string",
        "flatSearchCutoff": 1,
        "maxConnections": 1,
        "multivector": {
          "aggregation": "string",
          "enabled": true,
          "muvera": {
            "dprojections": 1,
            "enabled": true,
            "ksim": 1,
            "repetitions": 1
          }
        },
        "pq": {
          "bitCompression": true,
          "centroids": 1,
          "enabled": true,
          "encoder": {
            "distribution": "string",
            "type": "string"
          },
          "segments": 1,
          "trainingLimit": 1
        },
        "rq": {
          "bits": 1,
          "enabled": true,
          "rescoreLimit": 1
        },
        "skip": true,
        "skipDefaultQuantization": true,
        "sq": {
          "enabled": true,
          "rescoreLimit": 1,
          "trainingLimit": 1
        },
        "trackDefaultQuantization": true,
        "vectorCacheMaxObjects": 1
      },
      "vectorIndexType": "string",
      "vectorizer": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `class` | string |  |
| `invertedIndexConfig.bm25.b` | number |  |
| `invertedIndexConfig.bm25.k1` | number |  |
| `invertedIndexConfig.cleanupIntervalSeconds` | number |  |
| `invertedIndexConfig.stopwords.preset` | string |  |
| `invertedIndexConfig.usingBlockMaxWAND` | boolean |  |
| `multiTenancyConfig.autoTenantActivation` | boolean |  |
| `multiTenancyConfig.autoTenantCreation` | boolean |  |
| `multiTenancyConfig.enabled` | boolean |  |
| `properties[].dataType[]` | array<string> |  |
| `properties[].indexFilterable` | boolean |  |
| `properties[].indexRangeFilters` | boolean |  |
| `properties[].indexSearchable` | boolean |  |
| `properties[].name` | string |  |
| `properties[].tokenization` | string |  |
| `replicationConfig.asyncEnabled` | boolean |  |
| `replicationConfig.deletionStrategy` | string |  |
| `replicationConfig.factor` | number |  |
| `shardingConfig.actualCount` | number |  |
| `shardingConfig.actualVirtualCount` | number |  |
| `shardingConfig.desiredCount` | number |  |
| `shardingConfig.desiredVirtualCount` | number |  |
| `shardingConfig.function` | string |  |
| `shardingConfig.key` | string |  |
| `shardingConfig.strategy` | string |  |
| `shardingConfig.virtualPerPhysical` | number |  |
| `vectorIndexConfig.bq.enabled` | boolean |  |
| `vectorIndexConfig.cleanupIntervalSeconds` | number |  |
| `vectorIndexConfig.distance` | string |  |
| `vectorIndexConfig.dynamicEfFactor` | number |  |
| `vectorIndexConfig.dynamicEfMax` | number |  |
| `vectorIndexConfig.dynamicEfMin` | number |  |
| `vectorIndexConfig.ef` | number |  |
| `vectorIndexConfig.efConstruction` | number |  |
| `vectorIndexConfig.filterStrategy` | string |  |
| `vectorIndexConfig.flatSearchCutoff` | number |  |
| `vectorIndexConfig.maxConnections` | number |  |
| `vectorIndexConfig.multivector.aggregation` | string |  |
| `vectorIndexConfig.multivector.enabled` | boolean |  |
| `vectorIndexConfig.multivector.muvera.dprojections` | number |  |
| `vectorIndexConfig.multivector.muvera.enabled` | boolean |  |
| `vectorIndexConfig.multivector.muvera.ksim` | number |  |
| `vectorIndexConfig.multivector.muvera.repetitions` | number |  |
| `vectorIndexConfig.pq.bitCompression` | boolean |  |
| `vectorIndexConfig.pq.centroids` | number |  |
| `vectorIndexConfig.pq.enabled` | boolean |  |
| `vectorIndexConfig.pq.encoder.distribution` | string |  |
| `vectorIndexConfig.pq.encoder.type` | string |  |
| `vectorIndexConfig.pq.segments` | number |  |
| `vectorIndexConfig.pq.trainingLimit` | number |  |
| `vectorIndexConfig.rq.bits` | number |  |
| `vectorIndexConfig.rq.enabled` | boolean |  |
| `vectorIndexConfig.rq.rescoreLimit` | number |  |
| `vectorIndexConfig.skip` | boolean |  |
| `vectorIndexConfig.skipDefaultQuantization` | boolean |  |
| `vectorIndexConfig.sq.enabled` | boolean |  |
| `vectorIndexConfig.sq.rescoreLimit` | number |  |
| `vectorIndexConfig.sq.trainingLimit` | number |  |
| `vectorIndexConfig.trackDefaultQuantization` | boolean |  |
| `vectorIndexConfig.vectorCacheMaxObjects` | number |  |
| `vectorIndexType` | string |  |
| `vectorizer` | string |  |

## Native endpoint

Through the native Weaviate Vector Store API, this operation is `POST /v1/schema` (base URL `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-collection.md) for the provider-specific parameters and requirements.

