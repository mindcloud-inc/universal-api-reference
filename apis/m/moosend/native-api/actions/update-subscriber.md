# Update Subscriber with Moosend

Updates an existing subscriber in Moosend.

## Endpoint

- **Method:** `POST`
- **Path:** `/subscribers/{{MailingListID}}/update/{{SubscriberID}}.json`
- **Base URL:** `https://api.moosend.com/v3`
- **Official documentation:** [Update Subscriber](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54578-Update-a-subscriber?lang=en_US)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `MailingListID` | path | `string` | yes | The ID of the email list that contains the subscriber. |
| `SubscriberID` | path | `string` | yes | The ID of the subscriber that you want to update. |
| `Name` | body | `string` | no | The name of the subscriber. |
| `Email` | body | `string` | yes | The email address of the subscriber. |
| `HasExternalDoubleOptIn` | body | `boolean` | no | When true , it flags the added subscriber as having given subscription consent by other means. |
| `CustomFields` | body | `list<object>` | no | A list of name-value pairs that match the subscriber’s custom fields defined in the email list. For example, if you have two custom fields for Age and Country , you must specify the values for these two fields. |
| `Tags` | body | `object` | no | The member tag you can use to filter members by when working with an email list. |
| `Preferences` | body | `object` | no | The member preferences you can user to segment or filter members by, when working with an email list. |
