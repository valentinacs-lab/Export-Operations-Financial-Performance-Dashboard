# Export-Operations-Financial-Performance-Dashboard
Financial and quality analytics for export operations across multiple international clients.

 Export Operations & Financial Analytics
 
**Descripción:**
Dashboard financiero y de calidad para operaciones de exportación internacional, integrando información de ingresos y rechazos por cliente.

**Objetivos de negocio:**
- Monitorear ingresos por cliente y período
- Analizar variaciones financieras interanuales
- Evaluar impacto del rechazo de producto
- Facilitar reportes ejecutivos consolidados

**KPIs clave:**
- Ingresos totales
- Ingresos por cliente
- Variación porcentual de ingresos
- Porcentaje de rechazo
- Tendencia financiera

**Herramientas:**
Power BI · DAX · Financial Analytics · Data Quality Analysis


_ _ _ _ _

Medidas DAX

Ventas Totales USD =SUM ( Fact_Exportaciones[Ventas_USD] )

Rechazo Total USD =SUM ( Fact_Exportaciones[Rechazo_USD] )

% Rechazo =DIVIDE ( [Rechazo Total USD], [Ventas Totales USD] )

Ventas Año Anterior =CALCULATE ([Ventas Totales USD],SAMEPERIODLASTYEAR ( Dim_Fecha[Date] ))

Crecimiento YoY % =
DIVIDE ([Ventas Totales USD] - [Ventas Año Anterior],[Ventas Año Anterior])
