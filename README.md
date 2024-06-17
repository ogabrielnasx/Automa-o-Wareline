import time
import pyautogui as pa

with open ('codigos.txt') as codigos:
    for index, codigo in enumerate(codigos):

        partes = codigo.split(";")

        descricao_codigo = partes[0]
        procedimento_codigo = partes[1]
        valor = partes [2]

        #novo procedimento
        pa.doubleClick(x=3244,y=49)
        time.sleep(2)

        #s.h. padrão:
        pa.write(descricao_codigo)
        time.sleep(1)
        pa.press('ENTER')
        time.sleep(1)
        pa.press('TAB')
        time.sleep(1)

        #codigo s.h. proprio:
        pa.write(procedimento_codigo)
        time.sleep(1)
        pa.press('TAB')
        pa.press('TAB')
        pa.press('TAB')
        pa.press('TAB')
        pa.press('TAB')
        time.sleep(1)

        #valor sh
        pa.write(valor)
        time.sleep(1)
        #salvar
        pa.click(x=3056,y=176)
        time.sleep(2)

        #voltar
        pa.click(x=3131,y=54)
        time.sleep(2)
        pa.press('ENTER')
