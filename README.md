# Final_MineriaDeDatosI

FINAL MINERIA DE DATOS
-
Deberán leer el dataset de la siguiente manera:
url = "https://archive.ics.uci.edu/ml/machine-learning-databases/adult/adult.data"
columns = ['age', 'workclass', 'fnlwgt', 'education', 'education-num', 'marital-status', 'occupation', 'relationship', 'race', 'sex', 'capital-gain', 'capital-loss', 'hours-per-week', 'native-country', 'income']
df = pd.read_csv(url, names=columns, na_values=' ?', skipinitialspace=True)
Las características del dataset son las siguientes:
age (edad): La edad del individuo.
workclass (clase de trabajo): Una categoría que indica el tipo de empleo del individuo, por ejemplo, "Privado", "Autónomo", "Gobierno Estatal", etc.
fnlwgt (peso final): Este es un peso calculado por el Censo que indica el número de personas representadas por el individuo en el dataset. Es usado en análisis de muestras para hacer inferencias sobre la población.
education (nivel educativo): El nivel más alto de educación alcanzado por el individuo, por ejemplo, "Bachillerato", "Licenciatura", "Máster", etc.
education-num (número de educación): Una versión numérica del nivel educativo, donde los niveles de educación se codifican como números enteros.
marital-status (estado civil): El estado civil del individuo, por ejemplo, "Nunca casado", "Casado", "Divorciado", etc.
occupation (ocupación): El tipo de ocupación del individuo, por ejemplo, "Administrador", "Cocinero", "Profesor", etc.
relationship (relación): Describe la relación del individuo con otros miembros de la familia, por ejemplo, "Cónyuge", "Hijo/a", "Jefe/a de familia", etc.
race (raza): La raza del individuo, por ejemplo, "Blanco", "Negro", "Asiático", "Indio Americano", etc.
sex (sexo): El sexo del individuo, es decir, "Masculino" o "Femenino".
capital-gain (ganancia de capital): Ingreso adicional del individuo procedente de inversiones, ventas de activos, etc., en el último año.
capital-loss (pérdida de capital): Pérdida financiera del individuo procedente de inversiones, ventas de activos, etc., en el último año.
hours-per-week (horas por semana): El número de horas que el individuo trabaja por semana.
native-country (país de origen): El país de origen del individuo.
income (ingreso): El rango de ingresos del individuo, clasificado en dos categorías: <=50K para ingresos menores o iguales a 50,000 dólares anuales, y >50K para ingresos mayores a 50,000 dólares anuales.
PUNTOS A RESOLVER
1) Valores faltantes
a. ¿Cuántas filas tienen al menos un valor faltante? ¿Qué porcentaje representan sobre el total?
b. Eliminá esas filas. ¿Cuántas quedaron?
c. Desde lo teórico: ¿qué ventajas y desventajas tiene eliminar filas con valores faltantes? ¿Cuándo convendría imputar?
2) Outliers (valores atípicos)
a. Usá boxplots para detectar valores atípicos en las siguientes variables: age, hours-per-week, capital-gain, capital-loss.
b. Aplicá la técnica intercuartílica para contar cuántos valores atípicos hay en cada una.
c. Elegí una de estas variables y eliminá los outliers. Mostrá los gráficos antes y después. ¿Qué cambia?
3) Codificación del target y de variables categóricas
a. Codificá la variable income usando LabelEncoder y llamala income_encoded.
b. Aplicá OneHotEncoder a tres variables categóricas que consideres importantes. Justificá tu elección.
c. ¿Qué problema puede generar OneHotEncoder si una variable tiene muchas categorías?
4) División en entrenamiento y prueba
a. Separá el dataset en entrenamiento y prueba con la proporción que consideres adecuada.
b. ¿Qué puede pasar si usamos muy pocos datos para entrenar o muy pocos para testear?
5) Modelo: Árbol de Decisión
a. Entrená un DecisionTreeClassifier con random_state=42.
b. Mostrá: profundidad del árbol, cantidad de hojas y variables más importantes.
c. ¿Qué ventajas tiene este modelo? ¿En qué casos no lo recomendarías?
6) Evaluación del modelo
a. Calculá las métricas: accuracy, precision, recall, f1-score.
b. Mostrá la matriz de confusión.
c. Si estuvieras clasificando personas para recibir ayuda estatal, ¿qué métrica te parecería más importante? Justificá.
7) Exploración sin supervisión: DBSCAN
a. Elegí dos o tres variables numéricas para analizar patrones (por ejemplo: capital-gain, hours-per-week, age).
b. Aplicá el algoritmo DBSCAN para detectar agrupamientos automáticos. Indicá los parámetros usados (eps, min_samples).
c. Graficá los datos en un scatter plot, coloreando los puntos por los clusters encontrados.
d. ¿Qué observás? ¿DBSCAN logró identificar grupos diferenciados? ¿Coinciden con la variable income_encoded?
e. ¿Qué ventajas y limitaciones tiene DBSCAN para este tipo de análisis?
8) Variable fnlwgt
a. ¿Qué representa esta variable según la descripción del dataset?
b. ¿La dejarías para entrenar un modelo? Justificá tu decisión con tu propio criterio.
c. Mostrá su distribución y comentá brevemente qué observás.
9) Privacidad y anonimato
a. ¿Puede este dataset violar la privacidad aunque no tenga nombres? Explicá por qué.
b. Nombrá dos medidas simples que ayudarían a proteger más la privacidad si este dataset se hiciera público.
10) Discriminación y sesgos en datos
a. ¿Qué variables pueden introducir sesgos en modelos automáticos?
b. ¿Qué podría pasar si usás este dataset para predecir quién recibe un crédito bancario?
c. Proponé dos acciones concretas para reducir el riesgo de discriminación en este tipo de modelos.
