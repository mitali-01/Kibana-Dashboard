GET superstore_sales/_mapping

POST /superstore_sales/_search
{
  "query": {
    "exists": {
      "field": "City"
    }
  },
  "size": 0
}

POST /superstore_sales/_search
{
  "size": 0, 
  "aggs": {
    "sub_category_count": {
      "terms": {
        "field": "Sub-Category", 
        "size": 17
      }
    }
  }
}

POST /superstore_sales/_search
{
  "size": 0, 
  "aggs": {
    "sub_category_count": {
      "terms": {
        "field": "Category", 
        "size": 3
      }
    }
  }
}