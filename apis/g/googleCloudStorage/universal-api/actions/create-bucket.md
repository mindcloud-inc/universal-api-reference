# Google Cloud Storage: Create Bucket

Creates a new bucket in Google Cloud Storage.

```
POST https://connect.mindcloud.co/v1/universal/googleCloudStorage/latest/actions/create-bucket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Cloud Storage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleCloudStorage/latest/actions/create-bucket" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleCloudStorage/latest/actions/create-bucket', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Globally unique bucket name. |
| `location` | list<string> | no | Bucket location, such as US, EU, or a region. One of: `AFRICA-SOUTH1`, `ASIA`, `ASIA-EAST1`, `ASIA-EAST2`, `ASIA-NORTHEAST1`, `ASIA-NORTHEAST2`, `ASIA-NORTHEAST3`, `ASIA-SOUTH1`, `ASIA-SOUTH2`, `ASIA-SOUTHEAST1`, `ASIA-SOUTHEAST1-A`, `ASIA-SOUTHEAST1-B`, `ASIA-SOUTHEAST1-C`, `ASIA-SOUTHEAST2`, `ASIA-SOUTHEAST3`, `ASIA1`, `AUSTRALIA-SOUTHEAST1`, `AUSTRALIA-SOUTHEAST2`, `EU`, `EUR4`, `EUR5`, `EUR7`, `EUR8`, `EUROPE-CENTRAL2`, `EUROPE-NORTH1`, `EUROPE-NORTH2`, `EUROPE-SOUTHWEST1`, `EUROPE-WEST1`, `EUROPE-WEST1-B`, `EUROPE-WEST1-C`, `EUROPE-WEST1-D`, `EUROPE-WEST10`, `EUROPE-WEST12`, `EUROPE-WEST2`, `EUROPE-WEST3`, `EUROPE-WEST4`, `EUROPE-WEST6`, `EUROPE-WEST8`, `EUROPE-WEST9`, `ME-CENTRAL1`, `ME-CENTRAL2`, `ME-WEST1`, `NAM4`, `NORTHAMERICA-NORTHEAST1`, `NORTHAMERICA-NORTHEAST2`, `NORTHAMERICA-SOUTH1`, `SOUTHAMERICA-EAST1`, `SOUTHAMERICA-WEST1`, `US`, `US-CENTRAL1`, `US-CENTRAL1-A`, `US-CENTRAL1-B`, `US-CENTRAL1-C`, `US-CENTRAL1-F`, `US-EAST1`, `US-EAST4`, `US-EAST4-A`, `US-EAST4-B`, `US-EAST4-C`, `US-EAST5`, `US-EAST5-A`, `US-EAST5-B`, `US-EAST5-C`, `US-SOUTH1`, `US-WEST1`, `US-WEST2`, `US-WEST3`, `US-WEST4`, `US-WEST4-A`, `US-WEST4-B`, `US-WEST4-C`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `storageClass` | list<string> | no | Default storage class for new objects. One of: `ARCHIVE`, `COLDLINE`, `NEARLINE`, `RAPID`, `STANDARD`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "location": "string",
      "metageneration": "string",
      "name": "Ava Chen",
      "selfLink": "https://example.com",
      "storageClass": "string",
      "timeCreated": "2026-05-07T12:00:00.000Z",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `location` | string |  |
| `metageneration` | string |  |
| `name` | string |  |
| `selfLink` | string |  |
| `storageClass` | string |  |
| `timeCreated` | date |  |
| `updated` | date |  |

## Native endpoint

Through the native Google Cloud Storage API, this operation is `POST /storage/v1/b` (base URL `https://storage.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-bucket.md) for the provider-specific parameters and requirements.

