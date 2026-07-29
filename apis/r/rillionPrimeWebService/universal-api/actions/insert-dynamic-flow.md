# Rillion Prime Web Service: Insert Dynamic Flow

Insert a dynamic approval flow into the Prime register queue.

```
POST https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-dynamic-flow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime Web Service `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-dynamic-flow" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "dynamicFlow": {},
  "transferFromQueue": "true"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-dynamic-flow', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "dynamicFlow": {},
    "transferFromQueue": "true"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dynamicFlow` | object | yes | Fill in the fields below, or use Use Variables ({}) on this object to map the whole payload from a previous step. Field semantics: Prime Integration Tables, Dynamicflow section. |
| `transferFromQueue` | boolean | yes | Process the record from the queue immediately. Leave true unless your Rillion contact advises otherwise. Default: `true`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dynamicFlow.company` | list<string> | no | Company dynamic flow is for |
| `dynamicFlow.reduceFlow` | string | no | Activate reduced flow by setting value to 1. |
| `dynamicFlow.account` | string | no | Account or account interval flow is to be created for |
| `dynamicFlow.object1` | string | no | Object type 1 or object type 1 interval flow is to be created for |
| `dynamicFlow.object2` | string | no | Object type 2 or object type 2 interval flow is to be created for |
| `dynamicFlow.object3` | string | no | Object type 3 or object type 3 interval flow is to be created for |
| `dynamicFlow.object4` | string | no | Object type 4 or object type 4 interval flow is to be created for |
| `dynamicFlow.object5` | string | no | Object type 5 or object type 5 interval flow is to be created for |
| `dynamicFlow.object6` | string | no | Object type 6 or object type 6 interval flow is to be created for |
| `dynamicFlow.object7` | string | no | Object type 7 or object type 7 interval flow is to be created for |
| `dynamicFlow.object8` | string | no | Object type 8 or object type 8 interval flow is to be created for |
| `dynamicFlow.role1` | string | no | Name of role in level 1 of the dynamic flow |
| `dynamicFlow.role2` | string | no | Name of role in level 2 of the dynamic flow |
| `dynamicFlow.role3` | string | no | Name of role in level 3 of the dynamic flow |
| `dynamicFlow.role4` | string | no | Name of role in level 4 of the dynamic flow |
| `dynamicFlow.role5` | string | no | Name of role in level 5 of the dynamic flow |
| `dynamicFlow.role6` | string | no | Name of role in level 6 of the dynamic flow |
| `dynamicFlow.role7` | string | no | Name of role in level 7 of the dynamic flow |
| `dynamicFlow.role8` | string | no | Name of role in level 8 of the dynamic flow |
| `dynamicFlow.role9` | string | no | Name of role in level 9 of the dynamic flow |
| `dynamicFlow.role10` | string | no | Name of role in level 10 of the dynamic flow |
| `dynamicFlow.limit1` | number | no | Authorization amount limit for role in flow level 1. If left blank authorization amount will be set to 0.00 |
| `dynamicFlow.limit2` | number | no | Authorization amount limit for role in flow level 2. If left blank authorization amount will be set to 0.00. |
| `dynamicFlow.limit3` | number | no | Authorization amount limit for role in flow level 3. If left blank authorization amount will be set to 0.00. |
| `dynamicFlow.limit4` | number | no | Authorization amount limit for role in flow level 4. If left blank authorization amount will be set to 0.00. |
| `dynamicFlow.limit5` | number | no | Authorization amount limit for role in flow level 5. If left blank authorization amount will be set to 0.00. |
| `dynamicFlow.limit6` | number | no | Authorization amount limit for role in flow level 6. If left blank authorization amount will be set to 0.00. |
| `dynamicFlow.limit7` | number | no | Authorization amount limit for role in flow level 7. If left blank authorization amount will be set to 0.00. |
| `dynamicFlow.limit8` | number | no | Authorization amount limit for role in flow level 8. If left blank authorization amount will be set to 0.00. |
| `dynamicFlow.limit9` | number | no | Authorization amount limit for role in flow level 9. If left blank authorization amount will be set to 0.00. |
| `dynamicFlow.limit10` | number | no | Authorization amount limit for role in flow level 10. If left blank authorization amount will be set to 0.00. |
| `dynamicFlow.remove` | number | no | Should record be removed: 0=No; 1=Yes |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rillion Prime Web Service API returns.

## Native endpoint

Through the native Rillion Prime Web Service API, this operation is `POST` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/insert-dynamic-flow.md) for the provider-specific parameters and requirements.

