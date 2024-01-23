# RECOMENDACIONES DE ANALISTAS / TARGETS DE PRECIO

Otorga funcionalidades para obtener y procesar las recomendaciones de analistas del mercado sobre activos de renta variable. APIs de FMP Cloud y FinnHub.

## INDICE DE FUNCIONES:
- getAFRating(symbol, añoDesde, añoHasta, ponderacion = "igual", timeframe = "semanal"):
    Esta función permite obtener datos y graficar la evolución del rating de un activo por sus fundamentals según la API de FMP Cloud.
    Ofrece el puntaje según 5 ratios: 
        # - Valuación de Flujo de Fondos (DCF)
        # - Return on Equity (ROE)
        # - Return on Assets (ROA)
        # - Deuda sobre PN (DE)
        # - Precio sobre Ganancias (PER)
        # - Precio sobre Valor Libro (PB)
    Se puede setear año desde, año hasta y el tipo de ponderación:
    API de FMP Cloud.
    
- getRecommendationFH(symbol):
    Esta función devuelve las recomendaciones de los analistas para determinado activo según la API de FinnHub. Internamente trabaja un
    sistema de puntajes para obtener un valor en Base 10 (1 al 10) rankeando qué tan buenas perspectivas tiene el activo. Asimismo es
    posible consultar la data de la cantidad y porcentajes de opiniones en cada acción recomendada (strong buy, buy, hold, sell, strong sell).
