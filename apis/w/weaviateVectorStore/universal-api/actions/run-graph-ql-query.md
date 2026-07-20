# Weaviate Vector Store: Run GraphQL Query

Runs a GraphQL query in Weaviate.

```
GET https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/run-graph-ql-query
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Weaviate Vector Store `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/run-graph-ql-query?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/run-graph-ql-query?${params}`, {
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
| `query` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "Get": {
          "WizardSource20260410A": [
            {
              "status": "string",
              "targetRef": [
                {
                  "title": "string"
                }
              ],
              "title": "string"
            }
          ]
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.Get.WizardSource20260410A[].status` | string |  |
| `data.Get.WizardSource20260410A[].targetRef[].title` | string |  |
| `data.Get.WizardSource20260410A[].title` | string |  |

## Native endpoint

Through the native Weaviate Vector Store API, this operation is `POST /v1/graphql` (base URL `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-graph-ql-query.md) for the provider-specific parameters and requirements.

