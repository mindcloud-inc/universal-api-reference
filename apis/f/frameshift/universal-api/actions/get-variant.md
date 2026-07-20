# Frameshift: Get Variant

Retrieves detailed variant information from Frameshift.

```
GET https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/get-variant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frameshift `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/get-variant?connectionId=$CONNECTION_ID&projectId=string&variantId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "variantId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/get-variant?${params}`, {
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
| `projectId` | string | yes | Resource identifier for the project to access |
| `variantId` | string | yes | Resource identifier for the variant to access |
| `includeAnnotationData` | boolean | no | If true, the annotations for the variant will be included in the response |
| `includeGenotypeData` | boolean | no | If true, genotype data such as which samples are het or hom for this variant will be included in the response |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alt": "string",
      "chr": "string",
      "id": 1,
      "r_end": 1,
      "r_start": 1,
      "ref": "string",
      "var_type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alt` | string |  |
| `chr` | string |  |
| `id` | number |  |
| `r_end` | number |  |
| `r_start` | number |  |
| `ref` | string |  |
| `var_type` | string |  |

## Native endpoint

Through the native Frameshift API, this operation is `GET /v1/projects/:project_id/variants/:variant_id` (base URL `https://mosaic.frameshift.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-variant.md) for the provider-specific parameters and requirements.

