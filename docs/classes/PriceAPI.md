[ig-trading-api](../README.md) / [Exports](../modules.md) / PriceAPI

# Class: PriceAPI

## Table of contents

### Constructors

- [constructor](PriceAPI.md#constructor)

### Properties

- [URL](PriceAPI.md#url)

### Methods

- [getPrices](PriceAPI.md#getprices)
- [getPricesBetweenDates](PriceAPI.md#getpricesbetweendates)

## Constructors

### constructor

• **new PriceAPI**(`apiClient`)

#### Parameters

| Name        | Type            |
| :---------- | :-------------- |
| `apiClient` | `AxiosInstance` |

#### Defined in

[market/prices/PriceAPI.ts:86](https://github.com/bennycode/ig-trading-api/blob/c7d6810/src/market/prices/PriceAPI.ts#L86)

## Properties

### URL

▪ `Static` `Readonly` **URL**: `Object`

#### Type declaration

| Name     | Type     |
| :------- | :------- |
| `PRICES` | `string` |

#### Defined in

[market/prices/PriceAPI.ts:82](https://github.com/bennycode/ig-trading-api/blob/c7d6810/src/market/prices/PriceAPI.ts#L82)

## Methods

### getPrices

▸ **getPrices**(`epic`, `resolution`, `pointCount`, `pageSize?`, `pageNumber?`): `Promise`<[`HistoricalPricesResponse`](../interfaces/HistoricalPricesResponse.md)\>

Returns historical prices for a particular instrument.

#### Parameters

| Name | Type | Default value | Description |
| :-- | :-- | :-- | :-- |
| `epic` | `string` | `undefined` | Instrument identifier |
| `resolution` | [`Resolution`](../enums/Resolution.md) | `undefined` | Time resolution |
| `pointCount` | `number` | `undefined` | Limits the number of price points (not applicable if a date range has been specified) |
| `pageSize` | `number` | `0` | Number of candles per page of results (defaults to 0, no pagination) |
| `pageNumber` | `number` | `1` | Page of results to return (pagination) |

#### Returns

`Promise`<[`HistoricalPricesResponse`](../interfaces/HistoricalPricesResponse.md)\>

#### Defined in

[market/prices/PriceAPI.ts:130](https://github.com/bennycode/ig-trading-api/blob/c7d6810/src/market/prices/PriceAPI.ts#L130)

---

### getPricesBetweenDates

▸ **getPricesBetweenDates**(`epic`, `resolution`, `startDate`, `endDate`, `pageSize?`, `pageNumber?`): `Promise`<[`HistoricalPricesResponse`](../interfaces/HistoricalPricesResponse.md)\>

Returns historical prices between given dates.

**`note`** Uses the v3 API response

**`see`** https://labs.ig.com/rest-trading-api-reference/service-detail?id=521

#### Parameters

| Name | Type | Default value | Description |
| :-- | :-- | :-- | :-- |
| `epic` | `string` | `undefined` | Instrument identifier |
| `resolution` | [`Resolution`](../enums/Resolution.md) | `undefined` | Time resolution |
| `startDate` | `string` | `undefined` | Start date as ISO 8601 string, i.e. "2021-01-15T00:00:00.000Z" |
| `endDate` | `string` | `undefined` | End date as ISO 8601 string, i.e. "2021-01-16T00:00:00.000Z" |
| `pageSize` | `number` | `0` | Number of candles per page of results (defaults to 0, no pagination) |
| `pageNumber` | `number` | `1` | Page of results to return (pagination) |

#### Returns

`Promise`<[`HistoricalPricesResponse`](../interfaces/HistoricalPricesResponse.md)\>

#### Defined in

[market/prices/PriceAPI.ts:100](https://github.com/bennycode/ig-trading-api/blob/c7d6810/src/market/prices/PriceAPI.ts#L100)