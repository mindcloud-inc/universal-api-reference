# Send Sign Request with Stiply

Creates and sends a new sign request in Stiply.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/sign_requests`
- **Base URL:** `https://api.stiply.nl`
- **Official documentation:** [Send Sign Request](https://app.stiply.nl/api-documentation/v2#tag/sign-requests/operation/SendSignRequest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | The title of the sign request. |
| `subject` | body | `string` | no | The subject of the e-mail to the signers. |
| `message` | body | `string` | no | The message to be included in the e-mail to the signers. The message can have some basic HTML tags. The tags `<br>`, `<b>`, `<strong>`, `<i>`, `<em>`, `<u>`, `<a>`, `<ul>`, `<ol>`, `<li>`, `<p>`, `<h1-5>` are allowed. Always use `<br>` for newlines. |
| `signing_sequence_type` | body | `string` | no | Choose if all signers can sign in parallel or sequential. |
| `term` | body | `string` | no | 2 digit code representing the sign term (1d = one day, 2w = two weeks, 3m = three months). When omitted, the account's configured default term will be used. |
| `external_key` | body | `string` | no | A key for your internal use so you don't have to save the Stiply sign request key in your local database. However, your external key has to be unique. |
| `call_back_url` | body | `string` | no | An URL to be called by Stiply when the last signer has signed the document. Please note that `key={sign_request_key}`,`external_key={external_key}` and `sign_request_id={sign_request_id}` shall be added to the call back url querystring. The URL will be called using a `GET` request. When the callback responses with an error status code, the callback is retried 12 times using an exponential backoff algoritm. |
| `comment` | body | `string` | no | A comment for internal use. |
| `background_color_fields` | body | `string` | no | A background color for the fields that will be added to the documents.  Currently the following values are supported:  - null: transparent background (default) - #ffffff: white background |
| `account_id` | body | `string` | no | The id of the account to create the sign request in. The user must have permissions in the provided account.  When left empty, the default account of the user is used. |
| `file_urls[]` | body | `array<string>` | yes | — |
| `signers[]` | body | `array<object>` | yes | — |
| `signers[].email` | body | `string` | yes | The emailaddress of signer |
| `signers[].name` | body | `string` | no | The name of the signer |
| `signers[].role` | body | `string` | no | A signer can have different roles. Role is optional, but when provided can have the following values: ‘signer’, ‘approver’, ‘cc’, ‘dc’. When role is not provided the ‘signer’ role is used as default. When the value ‘signer’ is set, the signer will need to sign the document regularly. When the value ‘approver’ is set, the signer will need to approve the document without signing it. The approver role is only allowed when the signrequest has ‘signing_sequence_type’ set on ‘sequential’. When the value cc is set, the signer will be notified about the progress of the sign request and receive a copy of the signed documents. When the value dc is set, the signer will only receive the signed documents. |
| `signers[].allow_add_fields` | body | `boolean` | no | When true, the signer is allowed to add signature fields by clicking on the document. Please note that the sender is not required to add a signature field to the document when the signer is allowed to add fields. Can only be used in combination with role signer. |
| `signers[].auth_method` | body | `string` | no | Authentication method for signer.  - `sms`: signer is identified by sending a SMS with a code to a phone number - `idin`: signer is identified by using the trusted login method of a Dutch bank (receiving initials, surname, date of birth) - `idincomplete`: same as idin, but receiving additional data if available (gender, address, email address, phone number) - `emandate`: signer is requested to provide an electronic payment mandate using a Dutch bank account  When not provided, no identification of the signer will occur. |
| `signers[].invitation_method` | body | `string` | no | By default Stiply sends an email to the signer with a link to sign the sign request. If you would like to invite the signer yourself, you should set the invitation_method to `custom`. In that case Stiply shall not send an email with the sign request to the signer.  After sending the sign request use the [Get signers of the sign request](#tag/sign-requests/operation/GetSignRequestSigners) endpoint to get the sign requests's signers with sign link.  Use the value `self` for the first signer to use the Stiply 'self signing' feature. For more information on the 'self signing' feature, see our [article in the help center](https://help.stiply.com/nl/articles/260223-self-signing-zelf-ondertekenen-zonder-het-ondertekenproces-te-doorlopen).  When this property is not provided, Stiply will send an email to the signer. |
| `signers[].phone` | body | `string` | no | Cellular phone number of the signer is required in case auth_method is set to sms. |
| `signers[].language` | body | `string` | no | The language in which the signer receives correspondence. The options are: `da`, `de`, `en`, `es`, `fr`, `it`, `nl`, `pl`, `sv` |
| `signers[].subject` | body | `string` | no | You can send a specific message to a signer with a specific subject, that overrules the sign_request subject in the mail to the signer. |
| `signers[].message` | body | `string` | no | You can send a specific message to a signer, that overrules the sign_request message in the mail to the signer. The message can have some basic HTML tags. The tags `<br>`, `<b>`, `<strong>`, `<i>`, `<em>`, `<u>`, `<a>`, `<ul>`, `<ol>`, `<li>`, `<p>`, `<h1-5>` are allowed. Always use `<br>` for newlines. |
| `signers[].redirect_url` | body | `string` | no | The URL where this signer is redirected to after signing the documents. |
| `signers[].attachment_message` | body | `string` | no | This is the main message you can add when requesting attachments back from the signer. |
| `signers[].attachments[]` | body | `array<object>` | no | With this array you can ask the signer to sent some files back after signing. |
| `signers[].attachments[].description` | body | `string` | yes | This will be the short description of this specific attachment you want to receive from the signer. This could for example be a copy of a passport or a copy of their CV. |
| `signers[].attachments[].optional` | body | `boolean` | no | Mark the attachment optional. When the attachment is optional the signer is not required to provide this attachment. |
| `signers[].emandate` | body | `object` | no | — |
| `signers[].emandate.emandate_id` | body | `string` | no | Your own emandate identifier. If not set, Stiply will generate an emandate id for you. |
| `signers[].emandate.instrument_code` | body | `string` | yes | Type of emandate to request. Use CORE for default emandates, B2B for business to business emandates. CORE emandates have a refund risk of 56 days. Can be used for Consumer and Business debtors. B2B emandates don't have a refund risk period. Can only be used for Business debtors and are not supported by all banks. |
| `signers[].emandate.sequence_type` | body | `string` | yes | Sequence type for the emandate. Use RCUR for a recurring emandate and OOFF for a one-off emandate. |
| `signers[].emandate.max_amount` | body | `string` | no | The max amount of the emandate. Max amount is only used with a B2B emandate. |
| `signers[].fields[]` | body | `array<object>` | no | Array with fields for the signer |
| `signers[].fields[].name` | body | `string` | no | Name of the tag to search for in the documents. All occurences of the tag `{{name}}` are replaced by a field of the provided type. When a name is provided, the page, x and y are ignored. The occurences of the tag in the documents deteremine where the field will be placed. |
| `signers[].fields[].type` | body | `string` | yes | — |
| `signers[].fields[].field_group` | body | `string` | no | When the type is `radio`, all radiobutton fields with the same group will belong together. Making it required that you select one option within each group. |
| `signers[].fields[].width` | body | `string` | no | Width of the field. When not provided, the default width of the field type will be used. |
| `signers[].fields[].height` | body | `string` | no | Height of the field. When not provided, the default height of the field type will be used. |
| `signers[].fields[].document` | body | `string` | no | One based index of the document the field must be placed on. This value is required when the field must be placed by coordinates. |
| `signers[].fields[].page` | body | `string` | no | Page the field must be placed on. This value is required when the field must be placed by coordinates. |
| `signers[].fields[].x` | body | `string` | no | X-Position of the field This value is required when the field must be placed by coordinates. |
| `signers[].fields[].y` | body | `string` | no | Y-Position of the field This value is required when the field must be placed by coordinates. |
| `signers[].fields[].optional` | body | `string` | no | When true, the field is optional |
| `attachments[]` | body | `array<object>` | no | — |
| `attachments[].file_url` | body | `string` | yes | Url of the attachment |
| `attachments[].type` | body | `string` | yes | — |
