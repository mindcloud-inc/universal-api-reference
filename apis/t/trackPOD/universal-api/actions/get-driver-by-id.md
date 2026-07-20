# Track-POD: Get Driver By Id

Retrieves a driver from Track-POD by ID.

```
GET https://connect.mindcloud.co/v1/universal/trackPOD/latest/actions/get-driver-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Track-POD `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trackPOD/latest/actions/get-driver-by-id?connectionId=$CONNECTION_ID&id=18f0c81f-0f2d-4a38-a5ae-5a0c58f4c4c2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "18f0c81f-0f2d-4a38-a5ae-5a0c58f4c4c2"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trackPOD/latest/actions/get-driver-by-id?${params}`, {
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
| `id` | string | yes | Track-POD unique identifier for the driver. Example: `18f0c81f-0f2d-4a38-a5ae-5a0c58f4c4c2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Active": true,
      "Depot": "string",
      "DepotId": "string",
      "HomeAddress": "string",
      "Id": "string",
      "Name": "Ava Chen",
      "Note": "string",
      "Number": 1,
      "Phone": "string",
      "TeamCodes": [
        "string"
      ],
      "Username": "Ava Chen",
      "Vehicle": "string",
      "Zone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Active` | boolean | Active flag |
| `Depot` | string | Depot address |
| `DepotId` | string | Unique identifier in user accounting system |
| `HomeAddress` | string | Home address |
| `Id` | string | Track-POD unique identifier |
| `Name` | string | Name |
| `Note` | string | Note |
| `Number` | number | Sequence number |
| `Phone` | string | Phone |
| `TeamCodes` | array<string> | Team code |
| `Username` | string | Username |
| `Vehicle` | string | Vehicle number |
| `Zone` | string | Zone |

## Native endpoint

Through the native Track-POD API, this operation is `GET /Driver/Id/:id` (base URL `https://api.track-pod.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-driver-by-id.md) for the provider-specific parameters and requirements.

