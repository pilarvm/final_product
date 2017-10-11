# Función Tarjeta de crédito válida

Esta función confirma la validez del número de una tarjeta por medio del algoritmo de Luhn.  
El usuario ingresará su número de tarjeta y se mostrará una ventana emergente informando si el número es válido o no.

## Contenido  
* Archivos adjuntos.  
* Pseudocódigo de la función.  
* Diagrama de flujo.  

### Archivos adjuntos en repositorio
1. **Carpeta assets** contiene diagrama de flujo.
2. **Carpeta app** contiene archivo app.js en el cuál se ecuentra el código de la función con el lenguaje Javascript.    
3. **archivo index.html** está vinculado con app.js, el usuario podrá acceder a la función mediante este archivo.
4. **README.md** contiene pseudocódigo de la función.  


### Pseudocódigo de la función isValidCard

~~~
Funcion isValidCard ()
	sum <- 0
	Escribir numberCard
	Repetir
		Leer numberCard
		Para i<-0 Hasta numberCard.length Hacer
			Si (numberCard[i]=' ' O isNaN[numberCard[i]]) Entonces
				Escribir numberCard
			FinSi
		FinPara
	Hasta Que (numberCard.length<16 O numberCard.length>16)
	Para j<-0 Hasta numberCard.length Hacer
		charValue <- parseInt[numberCard[j]]
		Si j MOD 2<-0 Entonces
			sum <- sum+charValue
		FinSi
		Si j MOD 2<>0 Entonces
			Si ((charValue*2)<=9) Entonces
				sum <- sum+(charValue*2)
			FinSi
			Si ((charValue*2)>9) Entonces
				twoDigits <- charValue*2.toString
				sumDigits <- parseInt[twoDigits[0]]+parseInt[twoDigits[1]]
				sum <- sum+sumDigits
			FinSi
		FinSi
	FinPara
	Si sum MOD 10<-0 Entonces
		Escribir document.write['El número de su tarjeta es valido')
	SiNo
		Escribir document.write['El número de su tarjeta es inválido')
	FinSi
FinFuncion

Algoritmo tarjeta_de_credito
FinAlgoritmo

~~~
