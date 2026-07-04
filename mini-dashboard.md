# Mini Dashboard - Demo Sales Data

## Demo 说明

这是一个完全模拟的小型 ecommerce / retail 订单数据 demo，用于展示 Spreadsheet Cleanup + Mini Dashboard 服务的交付效果。它不是客户案例，不代表真实收入。

Dashboard 统计口径：

- 只统计 `duplicate_status = unique` 的订单。
- `Total Revenue` 只统计 `payment_status = Paid` 的订单金额。
- `Unpaid Orders` 包含 `Unpaid` 和 `Pending`，不包含 `Refunded`。

## KPI Summary

| Metric | Value |
| --- | ---: |
| Total Revenue | USD $1,544.50 |
| Total Orders | 50 |
| Paid Orders | 36 |
| Unpaid Orders | 12 |
| Refunded Orders | 2 |
| Duplicate Rows Excluded | 2 |

## Top 5 Products

| Rank | Product | Paid Revenue |
| ---: | --- | ---: |
| 1 | Desk Lamp | USD $270.00 |
| 2 | Keyboard | USD $165.00 |
| 3 | Notebook | USD $156.00 |
| 4 | Coffee Beans | USD $144.00 |
| 5 | Tea Box | USD $126.00 |

## Revenue by Category

| Category | Paid Revenue |
| --- | ---: |
| Electronics | USD $424.00 |
| Stationery | USD $306.00 |
| Home Office | USD $302.00 |
| Grocery | USD $270.00 |
| Accessories | USD $154.50 |
| Kitchen | USD $88.00 |

## Revenue by Country

| Country | Paid Revenue |
| --- | ---: |
| USA | USD $826.00 |
| UK | USD $256.00 |
| Canada | USD $211.50 |
| Singapore | USD $123.00 |
| Australia | USD $84.00 |
| Mexico | USD $44.00 |

## Data Quality Issues Fixed

| Issue Type | What Was Fixed |
| --- | --- |
| Inconsistent date formats | Standardized all dates to `YYYY-MM-DD`. |
| Extra spaces | Trimmed spaces in IDs, names, products, categories, countries, statuses and notes. |
| Text casing issues | Standardized product, category, country and payment status naming. |
| Payment status spelling | Standardized `PAID`, `paid`, `paid ` to `Paid`; `not paid`, `notpaid`, `un paid` to `Unpaid`. |
| Wrong totals | Recalculated `total_amount` from `quantity x unit_price`. |
| Missing values | Filled missing customer name as `Unknown Customer`; inferred one missing category from product. |
| Duplicate orders | Marked duplicate `order_id` rows as `duplicate_excluded` and excluded them from dashboard totals. |
| Messy notes | Trimmed and normalized notes without inventing new information. |

## Suggested Next Use

The cleaned CSV can be copied into Google Sheets or Excel. The dashboard metrics can be recreated as a summary tab or used as a short weekly sales snapshot.
