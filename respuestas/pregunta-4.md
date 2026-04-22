MATCH (p:Persona)-[:PARTICIPA_EN]->(pr:Proyecto)
WITH p, count(pr) AS totalProyectos
WHERE totalProyectos > 1
RETURN p.nombre