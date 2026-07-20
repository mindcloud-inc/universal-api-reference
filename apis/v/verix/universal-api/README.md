# <img src="https://images.mindcloud.co/apps/icons/verix_1774972807850.png" alt="Verix logo" width="28" height="28"> Verix: Universal API

Issue, manage, and retrieve verifiable digital credentials and credential groups in Verix.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/verix/latest
- **Category:** Human Resources / Learning (LMS)
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.verix.io
- **Vendor API docs:** https://docs.verix.io/verifiable_credentials_apis/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Groups](actions/list-groups.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/verix/latest/actions/list-groups?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Create Multiple Credentials](actions/create-multiple-credentials.md) | POST | Creates multiple credentials in Verix for a group. |
| [Delete Credential](actions/delete-credential.md) | DELETE | Deletes an unissued credential from Verix. |
| [Get Credential](actions/get-credential.md) | GET | Retrieves a credential from your Verix account. |
| [List Credentials](actions/list-credentials.md) | GET | Retrieves credentials from your Verix account. |
| [Update Multiple Credentials](actions/update-multiple-credentials.md) | PUT | Updates multiple credentials in Verix for a group. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Get Group](actions/get-group.md) | GET | Retrieves a credential group from Verix. |
| [List Groups](actions/list-groups.md) | GET | Retrieves credential groups from your Verix account. |

