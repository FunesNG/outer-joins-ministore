# outer-joins-ministore
-- Preguntas:

-- 1-¿Por qué usaste LEFT JOIN para la Consulta 1 y no INNER JOIN? ¿Qué se perdería si usaras INNER JOIN?
-- 2-¿Por qué usaste RIGHT JOIN para la Consulta 2? ¿Qué tabla está a la izquierda y cuál a la derecha en tu consulta?
-- 3-¿Qué representan los valores NULL en cada resultado? Explicá con un ejemplo concreto de los datos qué significa que venta_id sea NULL en la Consulta 1 y que producto_id de productos sea NULL en la Consulta 2.
--4-¿Cuándo usarías FULL OUTER JOIN en un caso real de negocio?


-- 1-Use LEFT JOIN para que me trajera todos los resultados de los productos que hay existentes. Si hubiese usado INNER JOIN solo me hubiese traido lo que coincidiera con la tabla ventas y no obtendria resultado para los productos que nunca se vendieron.

-- 2-Use RIGHT JOIN para que me trajera todos los resultados mas coincidencias de mi tabla derecha. De esta forma estoy viendo que una venta con un producto inexistente. En este caso mi tabla izquierda es PRODUCTOS y mi tabla derecha es VENTAS.

-- 3- Representan valores desconocidos o inexistentes.
-- En mi consulta 1 tengo NULL en venta_id dos productos que nunca se vendieron y en mi consulta 2 tengo un NULL en producto_id ya que se hizo una venta con un producto inexistente.

-- 4-Usaria FULL OUTER JOIN cuando necesite hacer una auditoria para ver un panorama completo de como esta todo. Tanto en el control de registro de ventas como en las ventas generales de los productos. De esta manera puedo detectar dos inconsistencias en una.
