//field name: delivery_time
//language: painless
//type: number

if (doc['Ship Date'].size() > 0 && doc['Order Date'].size() > 0) {
  return (doc['Ship Date'].value.toInstant().toEpochMilli() - doc['Order Date'].value.toInstant().toEpochMilli()) / (1000 * 60 * 60 * 24);
} else {
  return null;
}