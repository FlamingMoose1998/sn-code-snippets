function jsonToUnloadXml(table, json){
  // client side xml creator for unloads
  const xmlDoc = document.implementation.createDocument("", 'unload', null);
  const tableElement = xmlDoc.createElement(table);
  tableElement.setAttribute('action', 'INSERT_OR_UPDATE')
  xmlDoc.documentElement.appendChild(tableElement); 
  

  for (const field in json){
    const element = xmlDoc.createElement(field);
    element.textContent = json[field]
    tableElement.appendChild(element)
  }

  const serializer = new XMLSerializer();
  const xmlString = serializer.serializeToString(xmlDoc);

  return `<?xml version="1.0" encoding="UTF-8"?>${xmlString}`
}

const x = jsonToUnloadXml('x_221_fmqa_quiz', json)
console.log(x)
