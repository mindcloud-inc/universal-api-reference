# Insert Dynamic Flow with Rillion Prime Web Service

Insert a dynamic approval flow into the Prime register queue.

## Endpoint

- **Method:** `POST`
- **Base URL:** `{baseUrl}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `DynamicFlow` | body | `object` | yes | Fill in the fields below, or use Use Variables ({}) on this object to map the whole payload from a previous step. Field semantics: Prime Integration Tables, Dynamicflow section. |
| `DynamicFlow.Company` | body | `list<string>` | no | Company dynamic flow is for |
| `DynamicFlow.ReduceFlow` | body | `string` | no | Activate reduced flow by setting value to 1. |
| `DynamicFlow.Account` | body | `string` | no | Account or account interval flow is to be created for |
| `DynamicFlow.Object1` | body | `string` | no | Object type 1 or object type 1 interval flow is to be created for |
| `DynamicFlow.Object2` | body | `string` | no | Object type 2 or object type 2 interval flow is to be created for |
| `DynamicFlow.Object3` | body | `string` | no | Object type 3 or object type 3 interval flow is to be created for |
| `DynamicFlow.Object4` | body | `string` | no | Object type 4 or object type 4 interval flow is to be created for |
| `DynamicFlow.Object5` | body | `string` | no | Object type 5 or object type 5 interval flow is to be created for |
| `DynamicFlow.Object6` | body | `string` | no | Object type 6 or object type 6 interval flow is to be created for |
| `DynamicFlow.Object7` | body | `string` | no | Object type 7 or object type 7 interval flow is to be created for |
| `DynamicFlow.Object8` | body | `string` | no | Object type 8 or object type 8 interval flow is to be created for |
| `DynamicFlow.Role1` | body | `string` | no | Name of role in level 1 of the dynamic flow |
| `DynamicFlow.Role2` | body | `string` | no | Name of role in level 2 of the dynamic flow |
| `DynamicFlow.Role3` | body | `string` | no | Name of role in level 3 of the dynamic flow |
| `DynamicFlow.Role4` | body | `string` | no | Name of role in level 4 of the dynamic flow |
| `DynamicFlow.Role5` | body | `string` | no | Name of role in level 5 of the dynamic flow |
| `DynamicFlow.Role6` | body | `string` | no | Name of role in level 6 of the dynamic flow |
| `DynamicFlow.Role7` | body | `string` | no | Name of role in level 7 of the dynamic flow |
| `DynamicFlow.Role8` | body | `string` | no | Name of role in level 8 of the dynamic flow |
| `DynamicFlow.Role9` | body | `string` | no | Name of role in level 9 of the dynamic flow |
| `DynamicFlow.Role10` | body | `string` | no | Name of role in level 10 of the dynamic flow |
| `DynamicFlow.Limit1` | body | `number` | no | Authorization amount limit for role in flow level 1. If left blank authorization amount will be set to 0.00 |
| `DynamicFlow.Limit2` | body | `number` | no | Authorization amount limit for role in flow level 2. If left blank authorization amount will be set to 0.00. |
| `DynamicFlow.Limit3` | body | `number` | no | Authorization amount limit for role in flow level 3. If left blank authorization amount will be set to 0.00. |
| `DynamicFlow.Limit4` | body | `number` | no | Authorization amount limit for role in flow level 4. If left blank authorization amount will be set to 0.00. |
| `DynamicFlow.Limit5` | body | `number` | no | Authorization amount limit for role in flow level 5. If left blank authorization amount will be set to 0.00. |
| `DynamicFlow.Limit6` | body | `number` | no | Authorization amount limit for role in flow level 6. If left blank authorization amount will be set to 0.00. |
| `DynamicFlow.Limit7` | body | `number` | no | Authorization amount limit for role in flow level 7. If left blank authorization amount will be set to 0.00. |
| `DynamicFlow.Limit8` | body | `number` | no | Authorization amount limit for role in flow level 8. If left blank authorization amount will be set to 0.00. |
| `DynamicFlow.Limit9` | body | `number` | no | Authorization amount limit for role in flow level 9. If left blank authorization amount will be set to 0.00. |
| `DynamicFlow.Limit10` | body | `number` | no | Authorization amount limit for role in flow level 10. If left blank authorization amount will be set to 0.00. |
| `DynamicFlow.Remove` | body | `number` | no | Should record be removed: 0=No; 1=Yes |
| `TransferFromQueue` | body | `boolean` | yes | Process the record from the queue immediately. Leave true unless your Rillion contact advises otherwise. |
