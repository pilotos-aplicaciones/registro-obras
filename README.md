# Registro de Obras — RVC Constructora

App web para registro y gestión de proyectos de construcción. Parte del ecosistema **RVC Pilotos**.

## Descripción

Permite registrar obras con información completa: identificación, geometría por torre, departamentos por piso con tipología, y plazos contractuales.

## Funcionalidades

- **Registro de obras** con wizard de 4 pasos
- **Multi-torre**: cada proyecto puede tener 1 o más torres con datos independientes
- **Departamentos**: generación automática de nomenclatura (piso × 100 + N°), exclusión de deptos individuales
- **Tipología de deptos**: clasificación por dormitorios + baños + tipo de cocina (CK/CC)
- **Plazos**: oferta (manual), contrato y rectificado (calculados automáticamente de fechas)
- **Vista tarjetas** y **vista tabla** con filtros por Segmento, Ciudad y Comuna
- **Exportar Excel** compatible con base de comparación de presupuestos
- **Exportar / Importar JSON**
- **Carga de Excel** para importar datos existentes

## Acceso

Requiere cuenta Google autorizada en `plataforma_usuarios` (Firestore) con `apps: ['registro_obras']`.

## Tecnología

- HTML/CSS/JS — archivo único sin frameworks
- Firebase Firestore (colección `registro_obras_proyectos`)
- Firebase Authentication (Google OAuth)
- SheetJS para Excel
- Tipografía: DM Sans + DM Mono

## Proyecto Firebase

`rvc-pilotos-app` — mismo proyecto que Avance Obras y demás apps RVC.

## Dominio autorizado

Agregar en Firebase Console → Authentication → Settings → Authorized domains:
```
pilotos-aplicaciones.github.io
```

## Variables Firestore compatibles con Avance Obras

`nombre`, `zona`, `comuna`, `pisos`, `subterraneos`, `cantDeptosTipo`, `fechaInicioObra`, `departamentos[]`

---

*RVC Constructora · v2.1 · 2025*
