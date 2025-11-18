LEADS:
curl -X POST "https://sql1.srv869945.hstgr.cloud/webhook-test/lead-capture" -H "Content-Type: application/json" -d "{\"nombre\":\"Roberto\",\"apellido\":\"Director\",\"email\":\"roberto@cordsporacion-ejemplo.com\",\"telefono\":\"+3460011999888\",\"empresa\":\"Corporación Global S.A.\",\"interes\":\"Consultoría Premium\",\"mensaje\":\"Necesitamos implementar su solución urgentemente. Tenemos el presupuesto aprobado y buscamos empezar la próxima semana sin falta. Quedo a la espera de su llamada inmediata.\",\"fuente\":\"Google Ads\"}"
{"success":true,"message":"¡Gracias por tu interés! Te contactaremos pronto.","tiempo_respuesta":"48-72 horas"}

CHATBOT:
C:\Users\thePalms>curl -X POST https://sql1.srv869945.hstgr.cloud/webhook-test/webchat-message -H "Content-Type: application/json" -d "{\"message\":\"Hola, ¿cuáles son los precios de los paquetes?\",\"session_id\":\"sesion-prueba-001\",\"name\":\"Alex\",\"email\":\"alex@empresa.com\"}"
{"success":true,"message":"Hola Alex, ¡con gusto te informo sobre nuestros precios!\n\nTenemos el paquete Standard por $99/mes, el Premium por $199/mes y el NEXA por $399/mes. ¿Hay algún paquete que te interese conocer más a fondo?","session_id":"sesion-prueba-001","timestamp":"2025-11-18T22:19:33.584+01:00"}
C:\Users\thePalms>curl -X POST https://sql1.srv869945.hstgr.cloud/webhook-test/webchat-message -H "Content-Type: application/json" -d "{\"message\":\"que te habia preguntado antes?\",\"session_id\":\"sesion-prueba-001\",\"name\":\"Alex\",\"email\":\"alex@empresa.com\"}"
{"code":404,"message":"The requested webhook \"webchat-message\" is not registered.","hint":"Click the 'Execute workflow' button on the canvas, then try again. (In test mode, the webhook only works for one call after you click this button)"}
C:\Users\thePalms>curl -X POST https://sql1.srv869945.hstgr.cloud/webhook-test/webchat-message -H "Content-Type: application/json" -d "{\"message\":\"que te habia preguntado antes?\",\"session_id\":\"sesion-prueba-001\",\"name\":\"Alex\",\"email\":\"alex@empresa.com\"}"
{"success":true,"message":"Hola Alex, ¡claro! Anteriormente me preguntaste sobre los precios de nuestros paquetes.\n\nQuieres que te los repita o tienes alguna otra consulta?","session_id":"sesion-prueba-001","timestamp":"2025-11-18T22:20:34.593+01:00"}
C:\Users\thePalms>
