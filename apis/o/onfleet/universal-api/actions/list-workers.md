# Onfleet: List Workers

Retrieves a list of workers from Onfleet.

```
GET https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/list-workers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Onfleet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/list-workers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/list-workers?${params}`, {
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
      "accountStatus": "string",
      "activeTask": {},
      "additionalCapacities": {
        "capacityA": 1,
        "capacityB": 1,
        "capacityC": 1
      },
      "capacity": 1,
      "displayName": "Ava Chen",
      "id": "string",
      "imageUrl": {},
      "location": {},
      "name": "Ava Chen",
      "onDuty": true,
      "organization": "string",
      "phone": "string",
      "teams": [
        "string"
      ],
      "timeCreated": "2026-05-07T12:00:00.000Z",
      "timeLastModified": "2026-05-07T12:00:00.000Z",
      "timeLastSeen": {},
      "timezone": {},
      "vehicle": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountStatus` | string |  |
| `activeTask` | object |  |
| `additionalCapacities.capacityA` | number |  |
| `additionalCapacities.capacityB` | number |  |
| `additionalCapacities.capacityC` | number |  |
| `capacity` | number |  |
| `displayName` | string |  |
| `id` | string |  |
| `imageUrl` | object |  |
| `location` | object |  |
| `name` | string |  |
| `onDuty` | boolean |  |
| `organization` | string |  |
| `phone` | string |  |
| `teams[]` | string |  |
| `timeCreated` | date |  |
| `timeLastModified` | date |  |
| `timeLastSeen` | object |  |
| `timezone` | object |  |
| `vehicle` | object |  |

## Native endpoint

Through the native Onfleet API, this operation is `GET /workers` (base URL `https://onfleet.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workers.md) for the provider-specific parameters and requirements.

