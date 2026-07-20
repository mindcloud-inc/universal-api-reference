# Create Mailing List with Moosend

Creates a new mailing list in Moosend.

## Endpoint

- **Method:** `POST`
- **Path:** `/lists/create.json`
- **Base URL:** `https://api.moosend.com/v3`
- **Official documentation:** [Create Mailing List](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54570-Create-a-mailing-list?lang=en_US)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Name` | body | `string` | yes | The name of the email list. |
| `ConfirmationPage` | body | `string` | no | The URL of the page displayed at the end of the subscription process. |
| `RedirectAfterUnsubscribePage` | body | `string` | no | The URL of the redirect page when users unsubscribe from your email list. |
| `Preferences` | body | `list<object>` | yes | The Preferences field options. SelectType The data type of the field. Possible values can be SingleSelect or MultiSelect . Required field. Options Max options 10 IsRequired If the field is required. Default value false . |
| `PreferencePageId` | body | `string` | no | The preference page id. |
