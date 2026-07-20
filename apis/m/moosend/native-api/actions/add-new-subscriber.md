# Add New Subscriber with Moosend

Creates a new subscriber in Moosend.

## Endpoint

- **Method:** `POST`
- **Path:** `/subscribers/{{MailingListID}}/subscribe.json`
- **Base URL:** `https://api.moosend.com/v3`
- **Official documentation:** [Add New Subscriber](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54573-Add-a-new-subscriber?lang=en_US)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `MailingListID` | path | `string` | yes | The ID of the email list where you want to add a new subscriber. |
| `Name` | body | `string` | no | The name of the new subscriber. |
| `Email` | body | `string` | yes | The email address of the new subscriber. |
| `HasExternalDoubleOptIn` | body | `boolean` | no | When true , it flags the added subscriber as having given subscription consent by other means. |
| `CustomFields` | body | `list<object>` | no | A list of name-value pairs that match the subscriber’s custom fields defined in the email list. (for example, Name or Country ).  When updating an existing member, any custom fields that are not included in the request will have their values cleared. To preserve existing data, include values for all custom fields associated with the list. |
| `Tags` | body | `object` | no | The member tag you can use to filter members by when working with an email list. |
| `Preferences` | body | `object` | no | The member preferences you can use to segment or filter members by, when working with an email list. |
