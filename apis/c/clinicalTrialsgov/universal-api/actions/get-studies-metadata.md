# ClinicalTrials.gov: Get Studies Metadata



```
GET https://connect.mindcloud.co/v1/universal/clinicalTrialsgov/latest/actions/get-studies-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClinicalTrials.gov `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clinicalTrialsgov/latest/actions/get-studies-metadata?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clinicalTrialsgov/latest/actions/get-studies-metadata?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "children": [
        {}
      ],
      "name": "Ava Chen",
      "piece": "string",
      "sourceType": "string",
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `children` | array<object> | Nested child schema nodes. |
| `name` | string | Schema node name. |
| `piece` | string | ClinicalTrials.gov piece name. |
| `sourceType` | string | Underlying source type for the node. |
| `title` | string | Human-readable title for the field or section. |
| `type` | string | ClinicalTrials.gov data type for the node. |

## Native endpoint

Through the native ClinicalTrials.gov API, this operation is `GET /studies/metadata` (base URL `https://clinicaltrials.gov/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-studies-metadata.md) for the provider-specific parameters and requirements.

