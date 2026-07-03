# Sports 4 Dreams — Premium Web MVP

Plataforma web para recuperar equipamiento deportivo usado, registrar donantes, recibir solicitudes, gestionar inventario, mostrar impacto y crear trazabilidad por artículo.

## Diseño

Inspiración visual: propiedades deportivas premium tipo FIFA / Wimbledon:

- Hero oscuro con estética de estadio
- Verde institucional de alto contraste
- Métricas de impacto visibles
- Tarjetas de donación, solicitud y patrocinio
- Dashboard interno visual
- Página pública por código de equipo

## Stack

- Next.js App Router
- TypeScript
- PostgreSQL
- Prisma ORM
- Railway
- GitHub
- lucide-react para iconografía

## Setup local

```bash
npm install
cp .env.example .env
npx prisma migrate dev --name init
npm run dev
```

## Variables de entorno

```env
DATABASE_URL="postgresql://USER:PASSWORD@HOST:PORT/DATABASE"
NEXT_PUBLIC_APP_URL="http://localhost:3000"
ADMIN_EMAIL="admin@sports4dreams.org"
```

## Deploy en Railway

1. Crear un repositorio en GitHub.
2. Subir el contenido de este proyecto.
3. Crear un nuevo proyecto en Railway desde GitHub.
4. Agregar PostgreSQL en Railway.
5. Copiar `DATABASE_URL` al servicio web.
6. Ejecutar migraciones de Prisma.
7. Desplegar.

## Páginas incluidas

- `/` Landing premium
- `/donate` Formulario de donación
- `/request-support` Solicitud de apoyo
- `/sponsor` Formulario para patrocinadores
- `/dashboard` Dashboard interno básico
- `/item/[code]` Página pública de trazabilidad por equipo

## Próximo sprint recomendado

1. Autenticación admin.
2. Carga de fotos a almacenamiento externo.
3. Generación automática de QR.
4. Edición de estados del equipo desde dashboard.
5. Asignación de beneficiarios.
6. Reportes PDF para patrocinadores.
