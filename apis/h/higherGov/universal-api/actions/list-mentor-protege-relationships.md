# HigherGov: List Mentor Protege Relationships

Retrieves mentor-protege relationships from HigherGov.

```
GET https://connect.mindcloud.co/v1/universal/higherGov/latest/actions/list-mentor-protege-relationships
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HigherGov `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/higherGov/latest/actions/list-mentor-protege-relationships?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/higherGov/latest/actions/list-mentor-protege-relationships?${params}`, {
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
| `awardeeKeyMentor` | string | no | HigherGov Awardee Key of the mentor |
| `awardeeKeyMentorParent` | string | no | HigherGov Awardee Key of the mentor parent |
| `awardeeKeyProtege` | string | no | HigherGov Awardee Key of the protege |
| `awardeeKeyProtegeParent` | string | no | HigherGov Awardee Key of the protege parent |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active_flag": true,
      "awardee_key_mentor": {},
      "awardee_key_mentor_parent": {},
      "awardee_key_protege": {},
      "awardee_key_protege_parent": {},
      "primary_naics": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active_flag` | boolean |  |
| `awardee_key_mentor` | object |  |
| `awardee_key_mentor_parent` | object |  |
| `awardee_key_protege` | object |  |
| `awardee_key_protege_parent` | object |  |
| `primary_naics` | object |  |

## Native endpoint

Through the native HigherGov API, this operation is `GET /api-external/awardee-mp/` (base URL `https://www.highergov.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-mentor-protege-relationships.md) for the provider-specific parameters and requirements.

