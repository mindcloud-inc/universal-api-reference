# <img src="https://images.mindcloud.co/apps/icons/oneflow_1774300788631.jpeg" alt="Oneflow logo" width="28" height="28"> Oneflow: Universal API

Create, send, sign, and manage contracts with Oneflow

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/oneflow/latest
- **Category:** Productivity / Legal & Contracts
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://oneflow.com
- **Vendor API docs:** https://developer.oneflow.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Workspaces](actions/list-workspaces.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/list-workspaces?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Access Link

| Action | Method | Description |
| --- | --- | --- |
| [Create Access Link](actions/create-access-link.md) | POST | Creates an access link in Oneflow. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a contact in Oneflow. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves contact details from Oneflow. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from Oneflow. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Oneflow. |

### Contract

| Action | Method | Description |
| --- | --- | --- |
| [Create Contract](actions/create-contract.md) | POST | Creates a contract in Oneflow. |
| [Get Contract](actions/get-contract.md) | GET | Retrieves contract details from Oneflow. |
| [List Contracts](actions/list-contracts.md) | GET | Retrieves contracts from Oneflow. |
| [Publish Contract](actions/publish-contract.md) | PUT | Publishes a contract in Oneflow. |
| [Update Contract](actions/update-contract.md) | PUT | Updates an existing contract in Oneflow. |

### Contract Create Data

| Action | Method | Description |
| --- | --- | --- |
| [Get Contract Create Data](actions/get-contract-create-data.md) | GET | Retrieves contract creation data from Oneflow. |

### Data Field

| Action | Method | Description |
| --- | --- | --- |
| [List Contract Data Fields](actions/list-contract-data-fields.md) | GET | Retrieves contract data fields from Oneflow. |
| [Update Contract Data Field Value](actions/update-contract-data-field-value.md) | PUT | Updates a contract data field value in Oneflow. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Get Contract File](actions/get-contract-file.md) | GET | Retrieves contract file details from Oneflow. |
| [List Contract Files](actions/list-contract-files.md) | GET | Retrieves contract files from Oneflow. |

### Participant

| Action | Method | Description |
| --- | --- | --- |
| [Create Participant](actions/create-participant.md) | POST | Creates a contract participant in Oneflow. |

### Party

| Action | Method | Description |
| --- | --- | --- |
| [Create Party](actions/create-party.md) | POST | Creates a contract party in Oneflow. |
| [List Parties](actions/list-parties.md) | GET | Retrieves contract parties from Oneflow. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Get Template](actions/get-template.md) | GET | Retrieves template details from Oneflow. |
| [List Templates](actions/list-templates.md) | GET | Retrieves templates from Oneflow. |

### Template Type

| Action | Method | Description |
| --- | --- | --- |
| [Get Template Type](actions/get-template-type.md) | GET | Retrieves template type details from Oneflow. |
| [List Template Types](actions/list-template-types.md) | GET | Retrieves template types from Oneflow. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Retrieves users from Oneflow. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [List Workspaces](actions/list-workspaces.md) | GET | Retrieves workspaces from Oneflow. |

