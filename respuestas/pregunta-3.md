MATCH (p1:Persona)-[:TRABAJA_EN]->(e)<-[:TRABAJA_EN]-(p2:Persona) 
WHERE id(p1) < id(p2)
RETURN p1.nombre, p2.nombre