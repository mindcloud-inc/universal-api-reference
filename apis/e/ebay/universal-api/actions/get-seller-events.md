# eBay: Get Seller Events

Use this call to retrieve a list of the items on which a seller event has occurred. A seller event includes actions such as a revision to the item (e.g., a description change), a price change (through a bid), or the ending of an item's listing.

```
GET https://connect.mindcloud.co/v1/universal/ebay/latest/actions/get-seller-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eBay `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ebay/latest/actions/get-seller-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ebay/latest/actions/get-seller-events?${params}`, {
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
| `modTimeTo` | date | no |  |
| `modTimeFrom` | date | no |  |
| `startTimeFrom` | date | no |  |
| `startTimeTo` | date | no |  |
| `endTimeFrom` | date | no | Describes the earliest (oldest) date to use in a time range filter based on item end time. Must be specified if EndTimeTo is specified. |
| `endTimeTo` | date | no | Describes the latest (most recent) date to use in a time range filter based on item end time. If you specify the corresponding From filter, but you do not include EndTimeTo, then EndTimeTo is set to the time you make the call. |
| `newItemFilter` | boolean | no |  |
| `includeWatchCount` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Ack": "string",
      "Build": "string",
      "CorrelationID": "string",
      "Errors": [
        {
          "ErrorClassification": "string",
          "ErrorCode": "string",
          "ErrorParameters": [
            {
              "_ParamID": "string",
              "Value": [
                "string"
              ]
            }
          ],
          "LongMessage": "string",
          "SeverityCode": "string",
          "ShortMessage": "string"
        }
      ],
      "HardExpirationWarning": "string",
      "ItemArray": {
        "Item": [
          {
            "BestOfferDetails": {
              "BestOfferCount": 1,
              "BestOfferEnabled": true
            },
            "BuyItNowPrice": {
              "_currencyID": "string",
              "value": 1
            },
            "Currency": "string",
            "eBayPlus": true,
            "eBayPlusEligible": true,
            "HitCount": 1,
            "IsSecureDescription": true,
            "ItemID": "string",
            "ListingDetails": {
              "EndTime": "string",
              "StartTime": "string"
            },
            "ListingType": "string",
            "Quantity": 1,
            "SellerProfiles": {
              "SellerPaymentProfile": {
                "PaymentProfileID": 1,
                "PaymentProfileName": "Ava Chen"
              },
              "SellerReturnProfile": {
                "ReturnProfileID": 1,
                "ReturnProfileName": "Ava Chen"
              },
              "SellerShippingProfile": {
                "ShippingProfileID": 1,
                "ShippingProfileName": "Ava Chen"
              }
            },
            "SellerVacationNote": "string",
            "SellingStatus": {
              "BidCount": 1,
              "CurrentPrice": {
                "_currencyID": "string",
                "value": 1
              },
              "HighBidder": {
                "Email": "ava@example.com",
                "FeedbackScore": 1,
                "UserAnonymized": true,
                "UserID": "string"
              },
              "ListingStatus": "string",
              "QuantitySold": 1
            },
            "Site": "string",
            "Title": "string",
            "Variations": {
              "Variation": [
                {
                  "Quantity": 1,
                  "SellingStatus": {
                    "BidCount": 1,
                    "CurrentPrice": {
                      "_currencyID": "string",
                      "value": 1
                    },
                    "HighBidder": {
                      "Email": "ava@example.com",
                      "FeedbackScore": 1,
                      "UserAnonymized": true,
                      "UserID": "string"
                    },
                    "ListingStatus": "string",
                    "QuantitySold": 1
                  },
                  "SKU": "string",
                  "StartPrice": {
                    "_currencyID": "string",
                    "value": 1
                  },
                  "VariationProductListingDetails": {
                    "EAN": "string",
                    "ISBN": "string",
                    "UPC": "string"
                  },
                  "VariationSpecifics": {
                    "NameValueList": [
                      {
                        "Name": "Ava Chen",
                        "Value": [
                          "Ava Chen"
                        ]
                      }
                    ]
                  }
                }
              ]
            },
            "WatchCount": 1
          }
        ]
      },
      "Timestamp": "string",
      "TimeTo": "string",
      "Version": "string",
      "xmlns": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Ack` | string |  |
| `Build` | string |  |
| `CorrelationID` | string |  |
| `Errors[].ErrorClassification` | string |  |
| `Errors[].ErrorCode` | string |  |
| `Errors[].ErrorParameters[]._ParamID` | string |  |
| `Errors[].ErrorParameters[].Value[]` | string |  |
| `Errors[].LongMessage` | string |  |
| `Errors[].SeverityCode` | string |  |
| `Errors[].ShortMessage` | string |  |
| `HardExpirationWarning` | string |  |
| `ItemArray.Item[].BestOfferDetails.BestOfferCount` | number |  |
| `ItemArray.Item[].BestOfferDetails.BestOfferEnabled` | boolean |  |
| `ItemArray.Item[].BuyItNowPrice._currencyID` | string |  |
| `ItemArray.Item[].BuyItNowPrice.value` | number |  |
| `ItemArray.Item[].Currency` | string |  |
| `ItemArray.Item[].eBayPlus` | boolean |  |
| `ItemArray.Item[].eBayPlusEligible` | boolean |  |
| `ItemArray.Item[].HitCount` | number |  |
| `ItemArray.Item[].IsSecureDescription` | boolean |  |
| `ItemArray.Item[].ItemID` | string |  |
| `ItemArray.Item[].ListingDetails.EndTime` | string |  |
| `ItemArray.Item[].ListingDetails.StartTime` | string |  |
| `ItemArray.Item[].ListingType` | string |  |
| `ItemArray.Item[].Quantity` | number |  |
| `ItemArray.Item[].SellerProfiles.SellerPaymentProfile.PaymentProfileID` | number |  |
| `ItemArray.Item[].SellerProfiles.SellerPaymentProfile.PaymentProfileName` | string |  |
| `ItemArray.Item[].SellerProfiles.SellerReturnProfile.ReturnProfileID` | number |  |
| `ItemArray.Item[].SellerProfiles.SellerReturnProfile.ReturnProfileName` | string |  |
| `ItemArray.Item[].SellerProfiles.SellerShippingProfile.ShippingProfileID` | number |  |
| `ItemArray.Item[].SellerProfiles.SellerShippingProfile.ShippingProfileName` | string |  |
| `ItemArray.Item[].SellerVacationNote` | string |  |
| `ItemArray.Item[].SellingStatus.BidCount` | number |  |
| `ItemArray.Item[].SellingStatus.CurrentPrice._currencyID` | string |  |
| `ItemArray.Item[].SellingStatus.CurrentPrice.value` | number |  |
| `ItemArray.Item[].SellingStatus.HighBidder.Email` | string |  |
| `ItemArray.Item[].SellingStatus.HighBidder.FeedbackScore` | number |  |
| `ItemArray.Item[].SellingStatus.HighBidder.UserAnonymized` | boolean |  |
| `ItemArray.Item[].SellingStatus.HighBidder.UserID` | string |  |
| `ItemArray.Item[].SellingStatus.ListingStatus` | string |  |
| `ItemArray.Item[].SellingStatus.QuantitySold` | number |  |
| `ItemArray.Item[].Site` | string |  |
| `ItemArray.Item[].Title` | string |  |
| `ItemArray.Item[].Variations.Variation[].Quantity` | number |  |
| `ItemArray.Item[].Variations.Variation[].SellingStatus.BidCount` | number |  |
| `ItemArray.Item[].Variations.Variation[].SellingStatus.CurrentPrice._currencyID` | string |  |
| `ItemArray.Item[].Variations.Variation[].SellingStatus.CurrentPrice.value` | number |  |
| `ItemArray.Item[].Variations.Variation[].SellingStatus.HighBidder.Email` | string |  |
| `ItemArray.Item[].Variations.Variation[].SellingStatus.HighBidder.FeedbackScore` | number |  |
| `ItemArray.Item[].Variations.Variation[].SellingStatus.HighBidder.UserAnonymized` | boolean |  |
| `ItemArray.Item[].Variations.Variation[].SellingStatus.HighBidder.UserID` | string |  |
| `ItemArray.Item[].Variations.Variation[].SellingStatus.ListingStatus` | string |  |
| `ItemArray.Item[].Variations.Variation[].SellingStatus.QuantitySold` | number |  |
| `ItemArray.Item[].Variations.Variation[].SKU` | string |  |
| `ItemArray.Item[].Variations.Variation[].StartPrice._currencyID` | string |  |
| `ItemArray.Item[].Variations.Variation[].StartPrice.value` | number |  |
| `ItemArray.Item[].Variations.Variation[].VariationProductListingDetails.EAN` | string |  |
| `ItemArray.Item[].Variations.Variation[].VariationProductListingDetails.ISBN` | string |  |
| `ItemArray.Item[].Variations.Variation[].VariationProductListingDetails.UPC` | string |  |
| `ItemArray.Item[].Variations.Variation[].VariationSpecifics.NameValueList[].Name` | string |  |
| `ItemArray.Item[].Variations.Variation[].VariationSpecifics.NameValueList[].Value[]` | string |  |
| `ItemArray.Item[].WatchCount` | number |  |
| `Timestamp` | string |  |
| `TimeTo` | string |  |
| `Version` | string |  |
| `xmlns` | string |  |

## Native endpoint

Through the native eBay API, this operation is `POST` (base URL `https://api.ebay.com/ws/api.dll`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-seller-events.md) for the provider-specific parameters and requirements.

