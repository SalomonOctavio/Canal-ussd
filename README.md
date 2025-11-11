# Canal USSD (TELCO, 2016–2017)

Canal de autogestión Prepago habilitado vía USSD (*103#), con funcionalidades esenciales: consulta de saldo, número, bolsas activas y compra de datos. Reducción de carga al IVR y mejora de experiencia usuaria sin despliegue formal. Proyecto liderado como MVP funcional con integración OSB → PCRF/ICC.

---

## Contexto

El canal USSD estaba técnicamente disponible desde 2013, pero su habilitación fue postergada por reparos del área de CX y falta de alineación con IVR y WebApp. En 2016, se reactivó como iniciativa funcional enfocada en clientes Prepago, con decisión de simplificar funcionalidades y liberar sin comunicado formal.

---

## Objetivo

Habilitar un canal básico pero efectivo de autogestión para clientes Prepago, con foco en:
- Consulta de saldo (tiempo real)
- Visualización del número de línea
- Consulta de bolsas promocionales activas
- Compra directa de bolsas

---

## Enfoque funcional

- Menú USSD simplificado, alineado con WebApp.
- Configuración vía aplicativo interno (ING).
- Integración a sistemas core mediante OSB → PCRF (Huawei) y ICC (ALU/Nokia).
- Validación funcional, sin plan de comunicaciones ni ceremonia de lanzamiento.

---

## Resultado

- Adopción natural: ~30% de las ventas de bolsas Prepago migran al canal USSD.
- Reducción de carga al IVR (~80.000 llamadas/mes).
- Sin incidencias post-lanzamiento.
- TTGL corto y TTV inmediato.

---

## Aprendizajes

- La experiencia era esperada por los clientes: uso sin fricción.
- La ausencia de comunicación no fue crítica, pero un plan de adopción hubiese potenciado fidelización.
- USSD es un canal clave para prepago y bajo costo de soporte.

---

## Artefactos incluidos

📁 `/diagrams`  
- [`flujo-ussd.mmd`](./diagrams/flujo-ussd.mmd): flujo simplificado del menú y navegación USSD.
- [`arquitectura-ussd.mmd`](./diagrams/arquitectura-ussd.mmd): arquitectura funcional e integración del canal.

📁 `/docs`  
- [`kpis.md`](./docs/kpis.md): TTGL/TTV y resultados funcionales.

📁 `/uat`  
- [`plan-uat.md`](./uat/plan-uat.md): validación de menú, navegación e integración.  
- [`checklist-go-no-go.md`](./uat/checklist-go-no-go.md): criterios funcionales previos a liberación.

---

## Sistemas implicados

- Gateway USSD  
- OSB (Oracle Service Bus)  
- Huawei UPCC (PCRF)  
- ALU/Nokia ICC  
- Aplicativo de configuración ING