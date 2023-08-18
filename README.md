# Programa-de-desconto-do-INSS-por-salario
Código para executar o cálculo de desconto do INSS e Vale Transporte com base no salário bruto

salbrEX = float(input("Digite o valor do salário: "))

#Vale Transporte
if salbrEX <= 1320:
  final2 = salbrEX - (salbrEX/100)*7.5 - (salbrEX/100)*6.0
if salbrEX > 1320 and salbrEX <= 2571.29:
  final2 = salbrEX - (salbrEX/100)*9.0 - 19.80 - (salbrEX/100)*6.0
if salbrEX > 2571.29 and salbrEX <= 3856.94:
  final2 = salbrEX - (salbrEX/100)*12.0 - 96.94 - (salbrEX/100)*6.0
if salbrEX > 3856.94 and salbrEX < 7507.49:
  final2 = salbrEX - (salbrEX/100)*14.0 - 174.08 - (salbrEX/100)*6.0
if salbrEX > 7507.49:
  final2 = salbrEX - (salbrEX/100)*14.0 - 876.95 - (salbrEX/100)*6.0

#Sem Vale Transporte 
if salbrEX <= 1320:
  final1 = salbrEX - (salbrEX/100)*7.5
if salbrEX > 1320 and salbrEX <= 2571.29:
  final1 = salbrEX - (salbrEX/100)*9.0 - 19.80
if salbrEX > 2571.29 and salbrEX <= 3856.94:
  final1 = salbrEX - (salbrEX/100)*12.0 - 96.94
if salbrEX > 3856.94 and salbrEX < 7507.49:
  final1 = salbrEX - (salbrEX/100)*14.0 - 174.08
if salbrEX > 7507.49:
  final1 = salbrEX - (salbrEX/100)*14.0 - 876.95
    

  
print (f"Salário final com desconto do INSS:{final1}")
print (f"Salário final com desconto do INSS e Vale Transporte:{final2}")
