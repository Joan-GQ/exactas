[@goodUsernamesAreTaken](https://github.com/goodUsernamesAreTaken)

```haskell

--Ejercicios (Usar pares para representar vectores)

--Determina si tanto x e y se encuentran dentro de intervalos especificos
estanRelacionados :: (Float,Float) -> Bool
estanRelacionados (x,y) = (x <= 3 && y <=3) || ((x <= 7 && x>3) && (y <= 7 && y>3)) || (x>7 && y>7)

--Producto interno de 2 vectores de R2
prodInt :: (Float, Float) -> (Float,Float) -> Float
prodInt (x,y) (a,b) = x*a +y*b

--Devuelve True si la 1er coordenada del 1er vector es menor al del segundo
todoMenor :: (Float, Float) -> (Float,Float) -> Bool
todoMenor (a,b) (c,d) = a<c

--Devuelve la distancia entre dos puntos
distanciaPuntos :: (Float,Float) -> (Float,Float) ->Float
distanciaPuntos (a,b) (c,d) =sqrt((a-c)**2+(b-d)**2)

--Suma 3 numeros
sumaTerna :: Int-> Int -> Int-> Int
sumaTerna x y z = x + y + z
                  
--De una lista de 3 numeros, devuelve el primer numero par o devuelve 4                  
posicPrimerPar :: Int -> Int -> Int -> Int
posicPrimerPar x y z | x `mod` 2 == 0 = 1
                     | y `mod` 2 == 0 = 2
                     | z `mod` 2 == 0 = 3
                     |otherwise = 4  

--crea un vector a partir de un par de numeros
crearPar :: a-> b -> (a,b)
crearPar x y = (x,y)

--invierte el orden de un vector
invertir :: (a,b) -> (b,a)
invertir (x,y) = (y,x)

```

---

[@bdaugero](https://github.com/bdaugero)

```haskell
--Ejercicio 1:
estanRelacionados :: Float -> Float -> Bool
estanRelacionados x y | (x <= 3 && y <= 3) = True
                      | (x > 3 && y > 3) && (x <= 7 && y <= 7) = True
                      | (x > 7 && y >7) = True
                      | otherwise = False
                      
--Ejercicio 2:
prodInt :: (Float, Float) -> (Float, Float) -> Float
prodInt (a,b) (c,d) = (fst (a,b)) * (fst(c,d)) + (snd (a,b)) * (snd(c,d))

--Ejercicio 3:
todoMenor :: (Float, Float) -> (Float, Float) -> Bool
todoMenor (a,b) (c,d) = (fst (a,b) < (snd(c,d)))

--Ejercicio 4:
distanciaPuntos :: (Float, Float) -> (Float, Float) -> Float
distanciaPuntos (a, b) (c, d) = sqrt((fst(a, b) - fst(c, d))**2 + (snd(a, b) - snd(c, d))**2)

--Ejercicio 5:
sumaTerna :: (Int, Int, Int) -> Int
sumaTerna (a, b, c) = a + b + c

--Ejercicio 6:
posicPrimerPar :: (Int, Int, Int) -> Int
posicPrimerPar (a, b, c) | mod a 2 == 0 = 1
                         | mod b 2 == 0 = 2
                         | mod c 2 == 0 = 3
                         | otherwise = 4
                         
--Ejercicio 7:
crearPar :: a -> b -> (a, b)
crearPar x y = (x, y)

--Ejercicio 8: 
invertir :: (a, b) -> (b, a)
invertir (x, y) = (y, x)```
