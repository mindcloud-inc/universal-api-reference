# Zillow MLS Data: List agents

Retrieves agents from a Zillow MLS Data dataset.

```
GET https://connect.mindcloud.co/v1/universal/zillowMLSData/latest/actions/list-agents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zillow MLS Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zillowMLSData/latest/actions/list-agents?connectionId=$CONNECTION_ID&dataset=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dataset": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zillowMLSData/latest/actions/list-agents?${params}`, {
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
| `dataset` | string | yes | Bridge dataset code to read agents from. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "BridgeModificationTimestamp": "2026-05-07T12:00:00.000Z",
      "JobTitle": "string",
      "MemberCity": "string",
      "MemberFirstName": "Ava",
      "MemberFullName": "Ava Chen",
      "MemberKey": "string",
      "MemberLastName": "Chen",
      "MemberMlsId": "string",
      "MemberMobilePhone": "string",
      "MemberOfficePhone": "string",
      "MemberStateOrProvince": "string",
      "MemberStatus": "string",
      "MemberType": "string",
      "ModificationTimestamp": "2026-05-07T12:00:00.000Z",
      "OfficeKey": "string",
      "OfficeName": "Ava Chen",
      "OriginatingSystemName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `BridgeModificationTimestamp` | date | Last Bridge-side modification timestamp. |
| `JobTitle` | string | Member job title. |
| `MemberCity` | string | Member city. |
| `MemberFirstName` | string | Member first name. |
| `MemberFullName` | string | Member full name. |
| `MemberKey` | string | Primary member key. |
| `MemberLastName` | string | Member last name. |
| `MemberMlsId` | string | MLS member identifier. |
| `MemberMobilePhone` | string | Member mobile phone. |
| `MemberOfficePhone` | string | Member office phone. |
| `MemberStateOrProvince` | string | Member state or province. |
| `MemberStatus` | string | Member status. |
| `MemberType` | string | Member type. |
| `ModificationTimestamp` | date | Last member modification timestamp. |
| `OfficeKey` | string | Associated office key. |
| `OfficeName` | string | Associated office name. |
| `OriginatingSystemName` | string | Originating system name. |

## Native endpoint

Through the native Zillow MLS Data API, this operation is `GET /:dataset/agents` (base URL `https://api.bridgedataoutput.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-agents.md) for the provider-specific parameters and requirements.

