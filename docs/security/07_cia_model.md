# 07 — Mapa CIA (caso Pedidos) · Sesión 16

## Objetivo
Mapear controles reales S15/S16 a Confidentiality (C), Integrity (I) y Availability (A).

## Tabla de controles

| Control | C | I | A | Evidencia | Estado |
|---------|---|---|---|-----------|--------|
| Rol `app_readonly` / mínimo privilegio | ✓ | ✓ | | `permissions_test` S15 (o pendiente si no existe aún) | pendiente / real |
| TLS en tránsito | ✓ | ✓ | | `evidence/tls_test.txt` S16 | pendiente |
| Backup + restore | | ✓ | ✓ | `backup_restore` S15 | pendiente / real |
| Secret Manager (secreto fuera del repo) | ✓ | | | `evidence/secrets_test.txt` S16 | pendiente |
| Audit logs / logging | ✓ | ✓ | | `evidence/audit_test.txt` S16 | pendiente |
| Red / `pg_hba` (origen no autorizado denegado) | ✓ | | ✓ | `evidence/network_denied_test.txt` S16 | pendiente |
| Hardening before/after (menos superficie) | ✓ | | ✓ | `evidence/hardening_before.txt` + `hardening_after.txt` | pendiente |

## Lectura rápida
- **C (Confidentiality):** quién ve datos / secretos / canal cifrado.
- **I (Integrity):** que no se alteren datos ni permisos de más.
- **A (Availability):** backup/restore y que el servicio no quede expuesto de más.

## Nota
Las filas marcadas "pendiente" se actualizarán a evidencia real cuando pasen los gates de esta sesión.
