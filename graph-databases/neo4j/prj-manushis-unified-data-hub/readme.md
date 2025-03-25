The following will be used as the base schema for storing data within Neo4j of the root person (manushi)

3 properties will be used:
1. Person node - name, age, location, gender
2. Relationship node - type (friend, family, colleague), start_date, status of relationship (active, passive)
3. Data node - content, timestamp (when first data arrived), source (who shared the data)

Following will the relationships used in the cypher queries

(:Person)-[:IN_RELATIONSHIP_WITH]->(:Person)
(:Person)-[:SHARES_DATA]->(:Data)
(:Data)-[:ABOUT]->(:Person)
(:Relationship)-[:HAS_DATA]->(:Data)
