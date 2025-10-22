https://github.com/galonsopinilla-collab/agenda-telefonica-python.git# agenda-telefonica-python
agenda telefonica python

git config --global user.name "galonsopinilla-collab"
git config --global user.email "galonsopinilla@gmail.com"

name: Integración Continua
 
on:
  push:
    branches:
      - main
  pull_request:
    branches:
      - main
 
jobs:
  build:
    name: Ejecutar proceso de CI
    runs-on: ubuntu-latest
 
    steps:
      - name: 📥 Clonar el repositorio
        uses: actions/checkout@v4
 
      - name: 🏁 Mostrar mensaje de inicio
        run: echo "🚀 Iniciando proceso de Integración Continua en el repositorio..."
 
      - name: 🔍 Verificar entorno
        run: |
          echo "Sistema operativo: $(uname -a)"
          echo "Versión de Node (si está instalada):"
          node -v || echo "Node no está instalado"
 
      - name: ✅ Proceso de CI completado
        run: echo "✅ Integración Continua ejecutada correctamente."
