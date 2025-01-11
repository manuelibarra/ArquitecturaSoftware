### 1. Instalar linux en docker
user powe shell
````
docker pull ubuntu:20.04
docker run -it ubuntu:20.04 /bin/bash

````
### 2. Crear el primer pipeline
crea el archivo text.sh
````
#!/bin/bash

# Function to convert text to lowercase
convert_to_lowercase() {
  tr '[:upper:]' '[:lower:]'
}

# Function to count lines, words, and characters
count_statistics() {
  wc
}

# Input: read from a file or standard input
input() {
  if [ -f "$1" ]; then
    cat "$1"
  else
    echo "Input file not found. Reading from standard input."     
    cat
  fi
}

# Main function to run the pipeline
main() {
  input "$1" | convert_to_lowercase | count_statistics
}

# Run the main function with the first argument as input
main "$1"
```` 
crear el archivo de entreda textfile.txt
````
Ejemplo bash arquitectura de software pipeline
Este ejemplo es bastante simple y divide el proceso en tres etapas: entrada, procesamiento y salida.
Estamos procesando archivos de texto para convertir todo el texto a minúsculas y luego contar el número de líneas, palabras y caracteres.
````

### 3. Crear el segundo pipeline
### 4. Tarea pipeline