# <img src="https://images.mindcloud.co/apps/icons/dashform_1774894305072.png" alt="Dashform logo" width="28" height="28"> Dashform: Universal API

Build and manage AI-native forms with Dashform, including authenticated form administration through the Dashform API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dashform/latest
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://getaiform.com/
- **Vendor API docs:** https://github.com/makloai/dashform-cli-docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dashform/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Form

| Action | Method | Description |
| --- | --- | --- |
| [Create Form](actions/create-form.md) | POST | Creates a form in Dashform. |
| [Delete Form](actions/delete-form.md) | DELETE | Deletes a form from Dashform. |
| [Get Form](actions/get-form.md) | GET | Retrieves a form from Dashform. |
| [List Forms](actions/list-forms.md) | GET | Retrieves forms from Dashform. |
| [Update Form](actions/update-form.md) | PUT | Updates a form in Dashform. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Dashform. |

