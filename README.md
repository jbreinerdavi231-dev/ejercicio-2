# ejercicio-2
cantidad_estudiante = int(input("ingrese la cantidad de estudiante: "))

  aprobados = 0
  reprobados = 0
  suma_promedio = 0
  promedio_menor = 0
  promedio_mayor = 0

  for i in range(1 , cantidad_estudiante + 1) :
   print("estudiante{i}")

  nota1 = float(input("ingrese primera nota: "))
  nota2 = float(input("ingrese segunda nota: "))
  nota3 = float(input("ingrese tercera nota: "))

  while nota1 < 0 or nota1 > 5:
    print("la nota tiene que ser de 0.0 a 5.0")
    nota1 = float(input("ingrese otra ves la primera nota: "))


  while nota2 < 0 or nota2 > 5:
    print("la nota tiene que ser de 0.0 a 5.0")
    nota1 = float(input("ingrese otra ves la segunda nota: "))



  while nota3 < 0 or nota3 > 5:
    print("la nota tiene que ser de 0.0 a 5.0")
    nota1 = float(input("ingrese otra ves la tercera nota: "))

  promedio = (nota1 + nota2 + nota3 ) / 3

  print(f"promedio: {promedio}")

  if promedio < 3.0:
    print("calificacion reprobada")
    reprobados += 1

  elif promedio < 4.0:
    print("calificacion aprobado")
    aprobados += 1

  elif promedio <= 4.5:
    print("calificacion sobresaliente ")
    aprobados += 1

  else:
    print("calificacion exelente")
    aprobados += 1

  suma_promedio += promedio

  if promedio > promedio_mayor :
    promedio_mayor = promedio

  if promedio < promedio_menor :
    promedio_menor = promedio

promedio_general = suma_promedio / cantidad_estudiante

print("resultado")
print(f"cantidad de estudiantes aprobados: {aprobados}")
print(f"cantidad de estudiantes reprobados: {reprobados}")
print(f"promedio general del grupo: {promedio_general}")
print(f"promedio mas alto: {promedio_mayor}")
print(f"proemdio mas bajo: {promedio_menor}")
