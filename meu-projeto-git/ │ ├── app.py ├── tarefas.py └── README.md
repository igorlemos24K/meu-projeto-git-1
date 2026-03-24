tarefas = []

def adicionar_tarefa(nome):
    tarefa = {
        "nome": nome,
        "concluida": False
    }
    tarefas.append(tarefa)
    return tarefa

def listar_tarefas():
    return tarefas

def concluir_tarefa(index):
    if 0 <= index < len(tarefas):
        tarefas[index]["concluida"] = True
        return True
    return False 
    from tarefas import adicionar_tarefa, listar_tarefas, concluir_tarefa

# Simulando uso
adicionar_tarefa("Estudar Git")
adicionar_tarefa("Fazer projeto backend")

print("Tarefas:")
print(listar_tarefas())

concluir_tarefa(0)

print("Após concluir:")
print(listar_tarefas())
