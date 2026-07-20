# Ecwid Universal API Examples

These examples use the MindCloud API key and Ecwid connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Store Profile

Retrieves a store profile from Ecwid.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ecwid/latest/actions/get-store-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ecwid/latest/actions/get-store-profile?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "account": {
        "accountEmail": "ava@example.com",
        "accountName": "Ava Chen",
        "accountNickName": "Ava Chen",
        "availableFeatures": [
          "string"
        ],
        "brandName": "Ava Chen",
        "googlePlaySubscriptionsAvailable": true,
        "itunesSubscriptionsAvailable": true,
        "paid": true,
        "registrationDate": "2026-05-07T12:00:00.000Z",
        "supportEmail": "ava@example.com",
        "suspended": true,
        "trackStorefrontStats": true,
        "whiteLabel": true
      },
      "company": {
        "city": "string",
        "countryCode": "string",
        "email": "ava@example.com",
        "phone": "string",
        "postalCode": "string",
        "stateOrProvinceCode": "string"
      },
      "designSettings": {
        "enableCatalogOnOnePage": true,
        "enableCatalogSeamlessProductListView": true,
        "hideCategoryBlockShowAllEnabledProducts": true,
        "productDetailsAddToCartQuantityCompactView": true,
        "productDetailsDescriptionCompactView": true,
        "productDetailsEstimatedDeliveryTimeCompactView": true,
        "productDetailsExpandedGalleryLayout": "string",
        "productDetailsFavoritesCompactView": true,
        "productDetailsGalleryImagePosition": "string",
        "productDetailsGalleryLayout": "string",
        "productDetailsLayout": "string",
        "productDetailsPositionBreadcrumbs": 1,
        "productDetailsPositionBuyButton": 1,
        "productDetailsPositionProductDescription": 1,
        "productDetailsPositionProductName": 1,
        "productDetailsPositionProductOptions": 1,
        "productDetailsPositionProductPrice": 1,
        "productDetailsPositionProductSku": 1,
        "productDetailsPositionReviewSection": 1,
        "productDetailsPositionSaveForLater": 1,
        "productDetailsPositionShareButtons": 1,
        "productDetailsPositionSizeChart": 1,
        "productDetailsPositionSubtitle": 1,
        "productDetailsPositionWholesalePrices": 1,
        "productDetailsReviewsInSingleViewCompactView": true,
        "productDetailsShareButtonCompactView": true,
        "productDetailsShowAskQuestionSection": true,
        "productDetailsShowAttributes": true,
        "productDetailsShowBreadcrumbs": true,
        "productDetailsShowBreadcrumbsPosition": "string",
        "productDetailsShowDeliveryTime": true,
        "productDetailsShowImageAltTextAsVisibleDescription": true,
        "productDetailsShowInStockLabel": true,
        "productDetailsShowNavigationArrows": true,
        "productDetailsShowNumberOfItemsInStock": true,
        "productDetailsShowPricePerUnit": true,
        "productDetailsShowProductDescription": true,
        "productDetailsShowProductName": true,
        "productDetailsShowProductOptions": true,
        "productDetailsShowProductPhotoZoom": true,
        "productDetailsShowProductPrice": true,
        "productDetailsShowProductSku": true,
        "productDetailsShowQty": true,
        "productDetailsShowRatingSection": true,
        "productDetailsShowReviewsSection": true,
        "productDetailsShowReviewsSectionInOneCardView": true,
        "productDetailsShowSalePrice": true,
        "productDetailsShowSaveForLater": true,
        "productDetailsShowShareButtons": true,
        "productDetailsShowSubtitle": true,
        "productDetailsShowTax": true,
        "productDetailsShowWeight": true,
        "productDetailsShowWholesalePrices": true,
        "productDetailsStockPerOutletCompactView": true,
        "productDetailsTwoColumnsWithLeftSidebarShowProductDescriptionOnSidebar": true,
        "productDetailsTwoColumnsWithRightSidebarShowProductDescriptionOnSidebar": true,
        "productDetailsWholesalePricesCompactView": true,
        "productFiltersOpenedByDefaultOnCatalogPages": true,
        "productFiltersOpenedByDefaultOnCategoryPage": true,
        "productFiltersOrientation": "string",
        "productFiltersPositionCategoryPage": "string",
        "productFiltersPositionOnCatalogPages": "string",
        "productFiltersPositionSearchPage": "string",
        "productFiltersVisibleOnCatalogPages": true,
        "productListBuybuttonBehavior": "string",
        "productListCardSpacingType": "string",
        "productListCategoryTitleBehavior": "string",
        "productListImageAspectRatio": "string",
        "productListImageHasShadow": true,
        "productListImageSize": "string",
        "productListPriceBehavior": "string",
        "productListProductInfoLayout": "string",
        "productListRatingSectionBehavior": "string",
        "productListShowAdditionalImageOnHover": true,
        "productListShowFrame": true,
        "productListShowRatingInOneStar": true,
        "productListShowRatingNumberInFiveStarsView": true,
        "productListShowReviewsCountInFiveStarsView": true,
        "productListShowSortViewasOptions": true,
        "productListSizeProductOptionBehavior": "string",
        "productListSkuBehavior": "string",
        "productListSubtitlesBehavior": "string",
        "productListSwatchesProductOptionBehavior": "string",
        "productListTitleBehavior": "string",
        "shoppingCartProductsCollapsedOnDesktop": true,
        "shoppingCartProductsCollapsedOnMobile": true,
        "showBreadcrumbs": true,
        "showFooterMenu": true,
        "showSigninLink": true,
        "showSigninLinkWithUnifiedAccountPage": true,
        "swatchesProductOptionShape": "string",
        "swatchesProductOptionSize": "string"
      },
      "featureToggles": [
        {
          "enabled": true,
          "name": "Ava Chen",
          "visible": true
        }
      ],
      "formatsAndUnits": {
        "addressFormat": {
          "multiline": "string",
          "plain": "string"
        },
        "currency": "string",
        "currencyDecimalSeparator": "string",
        "currencyGroupSeparator": "string",
        "currencyPrecision": 1,
        "currencyPrefix": "string",
        "currencyRate": 1,
        "currencySuffix": "string",
        "currencyTruncateZeroFractional": true,
        "dateFormat": "string",
        "dimensionsUnit": "string",
        "orderNumberPrefix": "string",
        "orderNumberSuffix": "string",
        "timeFormat": "string",
        "timezone": "string",
        "volumeUnit": "string",
        "weightDecimalSeparator": "string",
        "weightGroupSeparator": "string",
        "weightTruncateZeroFractional": true,
        "weightUnit": "string"
      },
      "generalInfo": {
        "instantSiteV2Enabled": true,
        "profileId": "string",
        "starterSite": {
          "ecwidSubdomain": "string",
          "ecwidSubdomainSuffix": "string",
          "generatedUrl": "https://example.com",
          "slugsWithoutIdsEnabled": true
        },
        "storefrontUrlFormat": "https://example.com",
        "storefrontUrlSlugFormat": "https://example.com",
        "storeId": 1,
        "storeUrl": "https://example.com",
        "websitePlatform": "string"
      },
      "languages": {
        "defaultLanguage": "string",
        "enabledLanguages": [
          "string"
        ],
        "facebookPreferredLocale": "string"
      },
      "legalPagesSettings": {
        "legalPages": [
          {
            "display": "string",
            "displayTranslated": {
              "es": "string"
            },
            "enabled": true,
            "externalUrl": "https://example.com",
            "externalUrlTranslated": {
              "es": "https://example.com"
            },
            "text": "string",
            "textTranslated": {
              "es": "string"
            },
            "title": "string",
            "titleTranslated": {
              "es": "string"
            },
            "type": "string"
          }
        ],
        "requireTermsAgreementAtCheckout": true
      },
      "mailNotifications": {
        "adminMessages": {
          "lowStockNotification": {
            "enabled": true
          },
          "newOrderPlaced": {
            "enabled": true
          },
          "weeklyStatsReport": {
            "enabled": true
          }
        },
        "adminNotificationEmails": [
          "ava@example.com"
        ],
        "customerMarketingMessages": {
          "abandonedCartRecovery": {
            "enabled": true,
            "marketingBlockEnabled": true
          },
          "customerLoyaltyAppreciation": {
            "enabled": true
          },
          "favoriteProductsReminder": {
            "enabled": true
          },
          "feedbackRequest": {
            "enabled": true
          },
          "inactiveCustomerReminder": {
            "enabled": true
          },
          "purchaseAnniversary": {
            "enabled": true
          }
        },
        "customerNotificationFromEmail": "ava@example.com",
        "customerOrderMessages": {
          "downloadEgoods": {
            "enabled": true
          },
          "orderConfirmation": {
            "enabled": true,
            "marketingBlockEnabled": true
          },
          "orderDelivered": {
            "enabled": true
          },
          "orderIsReadyForPickup": {
            "enabled": true
          },
          "orderShipped": {
            "enabled": true
          },
          "orderStatusChanged": {
            "enabled": true
          }
        }
      },
      "payment": {
        "applePay": {
          "available": true,
          "enabled": true
        },
        "countryCode": "string",
        "paymentOptions": [
          {
            "appClientId": "string",
            "appNamespace": "Ava Chen",
            "checkoutDescription": "string",
            "checkoutTitle": "string",
            "checkoutTitleTranslated": {
              "es": "string"
            },
            "configured": true,
            "enabled": true,
            "id": "string",
            "instructionsForCustomer": {
              "instructions": "string",
              "instructionsTitle": "string",
              "instructionsTranslated": {
                "es": "string"
              }
            },
            "orderBy": 1,
            "paymentProcessorId": "string",
            "paymentProcessorTitle": "string"
          }
        ]
      },
      "productFiltersSettings": {
        "enabledInStorefront": true
      },
      "registrationAnswers": {
        "alreadySelling": "string",
        "ecom": "string",
        "forSomeone": "string",
        "goods": "string",
        "platform": "string",
        "pos": "string",
        "website": "string"
      },
      "settings": {
        "abandonedSales": {
          "autoAbandonedSalesRecovery": true
        },
        "acceptMarketingCheckboxCustomText": "string",
        "acceptMarketingCheckboxCustomTextTranslated": {
          "es": "string"
        },
        "acceptMarketingCheckboxDefaultValue": true,
        "askCompanyName": true,
        "askConsentToTrackInStorefront": true,
        "askTaxId": true,
        "askZipCode": true,
        "closed": true,
        "defaultAllProductsViewSortOrder": "string",
        "defaultProductSortOrder": "string",
        "favoritesEnabled": true,
        "googleRemarketingEnabled": true,
        "hideOutOfStockProductsInStorefront": true,
        "highlightCompositeProductsOnStorefront": "string",
        "linkUpEnabled": true,
        "openBagOnAddition": true,
        "orderCommentsCaption": "string",
        "orderCommentsCaptionTranslated": {
          "es": "string"
        },
        "orderCommentsEnabled": true,
        "orderCommentsRequired": true,
        "productCondition": "string",
        "productReviewsFeatureEnabled": true,
        "productSortOrderInCart": "string",
        "recurringSubscriptionsSettings": {
          "showRecurringSubscriptionsInControlPanel": true,
          "supportedPaymentMethodsStatuses": {
            "supportedPaymentMethodsAreAvailable": true,
            "supportedPaymentMethodsAreConnected": true
          }
        },
        "requirePhoneOnCheckout": true,
        "rootCategorySeoDescription": "string",
        "rootCategorySeoDescriptionTranslated": {
          "es": "string"
        },
        "rootCategorySeoTitleTranslated": {
          "es": "string"
        },
        "salePrice": {
          "displayDiscount": "string",
          "displayLowestPrice": true,
          "displayOnProductList": true,
          "oldPriceLabelTranslated": {
            "es": "string"
          }
        },
        "showAcceptMarketingCheckbox": true,
        "showPricePerUnit": true,
        "showRepeatOrderButton": true,
        "storeDescriptionTranslated": {
          "es": "string"
        },
        "storeName": "Ava Chen",
        "wixExternalTrackingEnabled": true
      },
      "shipping": {
        "handlingFee": {
          "value": 1
        },
        "shippingOrigin": {
          "city": "string",
          "countryCode": "string",
          "countryName": "Ava Chen",
          "phone": "string",
          "postalCode": "string",
          "stateOrProvinceCode": "string"
        }
      },
      "taxInvoiceSettings": {
        "attachTaxInvoiceToOrderEmailNotifications": "ava@example.com",
        "enableTaxInvoices": true,
        "generateInvoicesAutomatically": "string"
      },
      "taxSettings": {
        "automaticTaxEnabled": true,
        "b2bB2c": "string",
        "electronicInvoiceFieldsAtCheckoutEnabled": true,
        "euIossEnabled": true,
        "pricesIncludeTax": true,
        "taxExemptBusiness": true,
        "taxOnShippingCalculationScheme": "string",
        "ukVatRegistered": true
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Store Profile action reference](actions/get-store-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ecwid/latest/actions/get-store-profile).

## Adjust Product Stock

Updates product stock in Ecwid.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ecwid/latest/actions/adjust-product-stock" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "productId": 1,
  "quantityDelta": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ecwid/latest/actions/adjust-product-stock', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "productId": 1,
    "quantityDelta": 1
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Adjust Product Stock action reference](actions/adjust-product-stock.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ecwid/latest/actions/adjust-product-stock).
