# RPO/RTO - OBJETIVOS DE RECUPERACIÓN

## Estrategia de Continuidad del Negocio

Framework para definir y gestionar los objetivos de punto de recuperación (RPO) y tiempo de recuperación (RTO) de sistemas críticos.

## Definiciones Clave

- **[RPO - Recovery Point Objective](rpo/definition.md)** - Máxima pérdida de datos tolerable medida en tiempo
- **[RTO - Recovery Time Objective](rto/definition.md)** - Tiempo máximo aceptable de indisponibilidad del servicio
- **[MTPD - Maximum Tolerable Period of Disruption](mtpd/definition.md)** - Tiempo máximo antes de impacto irreversible
- **[WRT - Work Recovery Time](wrt/definition.md)** - Tiempo para restaurar operación normal completa

## Clasificación de Sistemas

| Sistema | Criticidad | RPO | RTO | Backup Freq | DR Strategy |
|---------|------------|-----|-----|-------------|-------------|
| **Core Banking** | Crítico | 0 min | 15 min | Continuo | Active-Active |
| **API Gateway** | Crítico | 5 min | 30 min | Cada 5 min | Active-Passive |
| **Customer Portal** | Alto | 1 hora | 2 horas | Cada hora | Warm Standby |
| **Analytics Platform** | Medio | 4 horas | 8 horas | Cada 4h | Cold Standby |
| **Dev/Test Environment** | Bajo | 24 horas | 48 horas | Diario | Backup Only |

## Estrategias de Backup

**[Backup Continuo](backup/continuous.md)** | **[Snapshots](backup/snapshots.md)** | **[Replicación Síncrona](backup/sync.md)** | **[Replicación Asíncrona](backup/async.md)**

## Testing y Validación

**Último DR Test**: 15 Oct 2024 | **Éxito Rate**: 97% | **Próximo Test**: 15 Ene 2025 | **[Ver Calendario Completo](testing/calendar.md)**

## Procedimientos de Recovery

**[Runbook Core Systems](recovery/core.md)** | **[Database Recovery](recovery/database.md)** | **[Application Recovery](recovery/apps.md)** | **[Network Recovery](recovery/network.md)**

## Métricas Actuales

**Cumplimiento RPO**: 98.5% | **Cumplimiento RTO**: 96.2% | **Backup Success Rate**: 99.7% | **Recovery Tests Passed**: 47/48

## Contacto Crisis Management

**Hotline 24x7**: +34 900 CRISIS | **War Room**: Sala 10.01 | **Email**: disaster.recovery@empresa.com | **[Escalation Matrix](contacts/escalation.md)**** | **[KPI Tracking](improve/kpis.md)**