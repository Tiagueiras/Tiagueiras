SELECT a.title, a.summary, a.content, a.created, a.category_id, a.member_id,
       c.name      AS category,
       CONCAT(m.forename, ' ', m.surname) AS author,
       i.file      AS image_file, 
       i.alt       AS image_alt 

  FROM article     AS a
  JOIN category    AS c   ON a.category_id = c.id
  JOIN member      AS m   ON a.member_id   = m.id
  LEFT JOIN image  AS i   ON a.image_id    = i.id

 WHERE a.id        = 22
   AND a.published = 1;

   --ESSE ARQUIVO CONSULTA O REPOSITÓRIO E SEUS DETALHES DE ACORDO COM AS ESPECIFICAÇÕE
   
