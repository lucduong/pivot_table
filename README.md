# Pivot Table
[![Build Status](https://travis-ci.org/lucduong/pivot_table.svg?branch=master)](http://travis-ci.org/lucduong/pivot_table)

### Info

- This gem is forked from `https://github.com/edjames/pivot_table`
- Add `extra_rows` for including some columns

### Installation

    gem install pivot_table

### Usage

Check the `edjames/pivot_table` repository for more details

```
    @ws = PivotTable::Grid.new(:include_columns => [:product_id, :price, :code]) do |g|
      g.source_data  = warehouses
      g.column_name  = :color_name
      g.row_name     = :product_name
      g.value_name   = :quantity
      g.field_name   = :quantity
    end
    @ws.build
```

```
@ws.extra_rows[0][:product_id] => Product ID of the first row
```
    

### Copyright

Copyright (c) 2014 Ed James. See LICENSE for details.
