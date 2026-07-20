# Trello: List Boards By Member

Retrieves boards for a member from Trello.

```
GET https://connect.mindcloud.co/v1/universal/trello/latest/actions/list-boards-by-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trello `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trello/latest/actions/list-boards-by-member?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trello/latest/actions/list-boards-by-member?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "closed": true,
      "creationMethod": {},
      "dateClosed": {},
      "dateLastActivity": "string",
      "dateLastView": "string",
      "datePluginDisable": {},
      "desc": "string",
      "descData": {},
      "enterpriseOwned": true,
      "id": "string",
      "idBoardSource": {},
      "idEnterprise": {},
      "idMemberCreator": "string",
      "idOrganization": "string",
      "ixUpdate": "string",
      "labelNames": {
        "black": "Ava Chen",
        "blackDark": "Ava Chen",
        "blackLight": "Ava Chen",
        "blue": "Ava Chen",
        "blueDark": "Ava Chen",
        "blueLight": "Ava Chen",
        "green": "Ava Chen",
        "greenDark": "Ava Chen",
        "greenLight": "Ava Chen",
        "lime": "Ava Chen",
        "limeDark": "Ava Chen",
        "limeLight": "Ava Chen",
        "orange": "Ava Chen",
        "orangeDark": "Ava Chen",
        "orangeLight": "Ava Chen",
        "pink": "Ava Chen",
        "pinkDark": "Ava Chen",
        "pinkLight": "Ava Chen",
        "purple": "Ava Chen",
        "purpleDark": "Ava Chen",
        "purpleLight": "Ava Chen",
        "red": "Ava Chen",
        "redDark": "Ava Chen",
        "redLight": "Ava Chen",
        "sky": "Ava Chen",
        "skyDark": "Ava Chen",
        "skyLight": "Ava Chen",
        "yellow": "Ava Chen",
        "yellowDark": "Ava Chen",
        "yellowLight": "Ava Chen"
      },
      "limits": {
        "attachments": {
          "perBoard": {
            "disableAt": 1,
            "status": "string",
            "warnAt": 1
          },
          "perCard": {
            "disableAt": 1,
            "status": "string",
            "warnAt": 1
          }
        },
        "boards": {
          "totalAccessRequestsPerBoard": {
            "disableAt": 1,
            "status": "string",
            "warnAt": 1
          },
          "totalMembersPerBoard": {
            "disableAt": 1,
            "status": "string",
            "warnAt": 1
          }
        },
        "cards": {
          "openPerBoard": {
            "disableAt": 1,
            "status": "string",
            "warnAt": 1
          },
          "openPerList": {
            "disableAt": 1,
            "status": "string",
            "warnAt": 1
          },
          "totalPerBoard": {
            "disableAt": 1,
            "status": "string",
            "warnAt": 1
          },
          "totalPerList": {
            "disableAt": 1,
            "status": "string",
            "warnAt": 1
          }
        },
        "checkItems": {
          "perChecklist": {
            "disableAt": 1,
            "status": "string",
            "warnAt": 1
          }
        },
        "checklists": {
          "perBoard": {
            "disableAt": 1,
            "status": "string",
            "warnAt": 1
          },
          "perCard": {
            "disableAt": 1,
            "status": "string",
            "warnAt": 1
          }
        },
        "customFieldOptions": {
          "perField": {
            "disableAt": 1,
            "status": "string",
            "warnAt": 1
          }
        },
        "customFields": {
          "perBoard": {
            "disableAt": 1,
            "status": "string",
            "warnAt": 1
          }
        },
        "labels": {
          "perBoard": {
            "disableAt": 1,
            "status": "string",
            "warnAt": 1
          }
        },
        "lists": {
          "openPerBoard": {
            "disableAt": 1,
            "status": "string",
            "warnAt": 1
          },
          "totalPerBoard": {
            "disableAt": 1,
            "status": "string",
            "warnAt": 1
          }
        },
        "reactions": {
          "perAction": {
            "disableAt": 1,
            "status": "string",
            "warnAt": 1
          },
          "uniquePerAction": {
            "disableAt": 1,
            "status": "string",
            "warnAt": 1
          }
        },
        "stickers": {
          "perCard": {
            "disableAt": 1,
            "status": "string",
            "warnAt": 1
          }
        }
      },
      "memberships": [
        {
          "deactivated": true,
          "id": "string",
          "idMember": "string",
          "memberType": "string",
          "unconfirmed": true
        }
      ],
      "name": "Ava Chen",
      "nodeId": "string",
      "pinned": true,
      "prefs": {
        "autoArchive": {},
        "background": "string",
        "backgroundBottomColor": "string",
        "backgroundBrightness": "string",
        "backgroundColor": {},
        "backgroundDarkColor": {},
        "backgroundDarkImage": {},
        "backgroundImage": "string",
        "backgroundImageScaled": [
          {
            "height": 1,
            "url": "https://example.com",
            "width": 1
          }
        ],
        "backgroundTile": true,
        "backgroundTopColor": "string",
        "calendarFeedEnabled": true,
        "canBeEnterprise": true,
        "canBeOrg": true,
        "canBePrivate": true,
        "canBePublic": true,
        "canInvite": true,
        "cardAging": "string",
        "cardCounts": true,
        "cardCovers": true,
        "comments": "string",
        "hideVotes": true,
        "invitations": "string",
        "isTemplate": true,
        "permissionLevel": "string",
        "selfJoin": true,
        "sharedSourceUrl": "https://example.com",
        "showCompleteStatus": true,
        "switcherViews": [
          {
            "enabled": true,
            "viewType": "string"
          }
        ],
        "voting": "string"
      },
      "premiumFeatures": [
        "string"
      ],
      "shortLink": "https://example.com",
      "shortUrl": "https://example.com",
      "starred": true,
      "subscribed": true,
      "templateGallery": {},
      "type": {},
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `closed` | boolean |  |
| `creationMethod` | object |  |
| `dateClosed` | object |  |
| `dateLastActivity` | string |  |
| `dateLastView` | string |  |
| `datePluginDisable` | object |  |
| `desc` | string |  |
| `descData` | object |  |
| `enterpriseOwned` | boolean |  |
| `id` | string |  |
| `idBoardSource` | object |  |
| `idEnterprise` | object |  |
| `idMemberCreator` | string |  |
| `idOrganization` | string |  |
| `ixUpdate` | string |  |
| `labelNames.black` | string |  |
| `labelNames.blackDark` | string |  |
| `labelNames.blackLight` | string |  |
| `labelNames.blue` | string |  |
| `labelNames.blueDark` | string |  |
| `labelNames.blueLight` | string |  |
| `labelNames.green` | string |  |
| `labelNames.greenDark` | string |  |
| `labelNames.greenLight` | string |  |
| `labelNames.lime` | string |  |
| `labelNames.limeDark` | string |  |
| `labelNames.limeLight` | string |  |
| `labelNames.orange` | string |  |
| `labelNames.orangeDark` | string |  |
| `labelNames.orangeLight` | string |  |
| `labelNames.pink` | string |  |
| `labelNames.pinkDark` | string |  |
| `labelNames.pinkLight` | string |  |
| `labelNames.purple` | string |  |
| `labelNames.purpleDark` | string |  |
| `labelNames.purpleLight` | string |  |
| `labelNames.red` | string |  |
| `labelNames.redDark` | string |  |
| `labelNames.redLight` | string |  |
| `labelNames.sky` | string |  |
| `labelNames.skyDark` | string |  |
| `labelNames.skyLight` | string |  |
| `labelNames.yellow` | string |  |
| `labelNames.yellowDark` | string |  |
| `labelNames.yellowLight` | string |  |
| `limits.attachments.perBoard.disableAt` | number |  |
| `limits.attachments.perBoard.status` | string |  |
| `limits.attachments.perBoard.warnAt` | number |  |
| `limits.attachments.perCard.disableAt` | number |  |
| `limits.attachments.perCard.status` | string |  |
| `limits.attachments.perCard.warnAt` | number |  |
| `limits.boards.totalAccessRequestsPerBoard.disableAt` | number |  |
| `limits.boards.totalAccessRequestsPerBoard.status` | string |  |
| `limits.boards.totalAccessRequestsPerBoard.warnAt` | number |  |
| `limits.boards.totalMembersPerBoard.disableAt` | number |  |
| `limits.boards.totalMembersPerBoard.status` | string |  |
| `limits.boards.totalMembersPerBoard.warnAt` | number |  |
| `limits.cards.openPerBoard.disableAt` | number |  |
| `limits.cards.openPerBoard.status` | string |  |
| `limits.cards.openPerBoard.warnAt` | number |  |
| `limits.cards.openPerList.disableAt` | number |  |
| `limits.cards.openPerList.status` | string |  |
| `limits.cards.openPerList.warnAt` | number |  |
| `limits.cards.totalPerBoard.disableAt` | number |  |
| `limits.cards.totalPerBoard.status` | string |  |
| `limits.cards.totalPerBoard.warnAt` | number |  |
| `limits.cards.totalPerList.disableAt` | number |  |
| `limits.cards.totalPerList.status` | string |  |
| `limits.cards.totalPerList.warnAt` | number |  |
| `limits.checkItems.perChecklist.disableAt` | number |  |
| `limits.checkItems.perChecklist.status` | string |  |
| `limits.checkItems.perChecklist.warnAt` | number |  |
| `limits.checklists.perBoard.disableAt` | number |  |
| `limits.checklists.perBoard.status` | string |  |
| `limits.checklists.perBoard.warnAt` | number |  |
| `limits.checklists.perCard.disableAt` | number |  |
| `limits.checklists.perCard.status` | string |  |
| `limits.checklists.perCard.warnAt` | number |  |
| `limits.customFieldOptions.perField.disableAt` | number |  |
| `limits.customFieldOptions.perField.status` | string |  |
| `limits.customFieldOptions.perField.warnAt` | number |  |
| `limits.customFields.perBoard.disableAt` | number |  |
| `limits.customFields.perBoard.status` | string |  |
| `limits.customFields.perBoard.warnAt` | number |  |
| `limits.labels.perBoard.disableAt` | number |  |
| `limits.labels.perBoard.status` | string |  |
| `limits.labels.perBoard.warnAt` | number |  |
| `limits.lists.openPerBoard.disableAt` | number |  |
| `limits.lists.openPerBoard.status` | string |  |
| `limits.lists.openPerBoard.warnAt` | number |  |
| `limits.lists.totalPerBoard.disableAt` | number |  |
| `limits.lists.totalPerBoard.status` | string |  |
| `limits.lists.totalPerBoard.warnAt` | number |  |
| `limits.reactions.perAction.disableAt` | number |  |
| `limits.reactions.perAction.status` | string |  |
| `limits.reactions.perAction.warnAt` | number |  |
| `limits.reactions.uniquePerAction.disableAt` | number |  |
| `limits.reactions.uniquePerAction.status` | string |  |
| `limits.reactions.uniquePerAction.warnAt` | number |  |
| `limits.stickers.perCard.disableAt` | number |  |
| `limits.stickers.perCard.status` | string |  |
| `limits.stickers.perCard.warnAt` | number |  |
| `memberships[].deactivated` | boolean |  |
| `memberships[].id` | string |  |
| `memberships[].idMember` | string |  |
| `memberships[].memberType` | string |  |
| `memberships[].unconfirmed` | boolean |  |
| `name` | string |  |
| `nodeId` | string |  |
| `pinned` | boolean |  |
| `prefs.autoArchive` | object |  |
| `prefs.background` | string |  |
| `prefs.backgroundBottomColor` | string |  |
| `prefs.backgroundBrightness` | string |  |
| `prefs.backgroundColor` | object |  |
| `prefs.backgroundDarkColor` | object |  |
| `prefs.backgroundDarkImage` | object |  |
| `prefs.backgroundImage` | string |  |
| `prefs.backgroundImageScaled[].height` | number |  |
| `prefs.backgroundImageScaled[].url` | string |  |
| `prefs.backgroundImageScaled[].width` | number |  |
| `prefs.backgroundTile` | boolean |  |
| `prefs.backgroundTopColor` | string |  |
| `prefs.calendarFeedEnabled` | boolean |  |
| `prefs.canBeEnterprise` | boolean |  |
| `prefs.canBeOrg` | boolean |  |
| `prefs.canBePrivate` | boolean |  |
| `prefs.canBePublic` | boolean |  |
| `prefs.canInvite` | boolean |  |
| `prefs.cardAging` | string |  |
| `prefs.cardCounts` | boolean |  |
| `prefs.cardCovers` | boolean |  |
| `prefs.comments` | string |  |
| `prefs.hideVotes` | boolean |  |
| `prefs.invitations` | string |  |
| `prefs.isTemplate` | boolean |  |
| `prefs.permissionLevel` | string |  |
| `prefs.selfJoin` | boolean |  |
| `prefs.sharedSourceUrl` | string |  |
| `prefs.showCompleteStatus` | boolean |  |
| `prefs.switcherViews[].enabled` | boolean |  |
| `prefs.switcherViews[].viewType` | string |  |
| `prefs.voting` | string |  |
| `premiumFeatures[]` | string |  |
| `shortLink` | string |  |
| `shortUrl` | string |  |
| `starred` | boolean |  |
| `subscribed` | boolean |  |
| `templateGallery` | object |  |
| `type` | object |  |
| `url` | string |  |

## Native endpoint

Through the native Trello API, this operation is `GET members/:id/boards` (base URL `https://api.trello.com/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-boards-by-member.md) for the provider-specific parameters and requirements.

