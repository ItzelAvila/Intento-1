# Pr-ctica-1
ItzelAvila
def es_secuencia_bien_formada(cadena):
    pila = []
    for caracter in cadena:
        if caracter == '(':
            pila.append(caracter)
        elif caracter == ')':
            if not pila:
                return False  # Se encontró un ')' sin un '(' correspondiente
            pila.pop()
    return not pila  # La pila debe estar vacía al final si la secuencia es bien formada


# Ejemplo de uso
cadena = input("Ingrese una secuencia de paréntesis: ")
if es_secuencia_bien_formada(cadena):
    print("La secuencia de paréntesis está bien formada.")
else:
    print("La secuencia de paréntesis NO está bien formada.") 
