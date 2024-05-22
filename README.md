# atividade-11
João Guilherme Gomes Sanna

ATIVIDADE 01

#include <iostream>
#include <string>

using namespace std;

const int MAX_ALUNOS = 5;
const int NUM_NOTAS = 4;

// Definição da estrutura Aluno
struct Aluno {
    string nome;
    int idade;
    float notas[NUM_NOTAS];
};

// Função para verificar se uma nota está no intervalo válido (0 a 10)
bool verificarNota(float nota) {
    return (nota >= 0 && nota <= 10);
}

int main() {
    Aluno alunos[MAX_ALUNOS];
    int numAlunos = 0;
    int opcao;

    do {
        cout << "\nSelecione uma opcao:\n";
        cout << "1. Cadastrar novo aluno\n";
        cout << "2. Listar alunos cadastrados\n";
        cout << "3. Sair\n";
        cout << "Opcao: ";
        cin >> opcao;

        switch (opcao) {
            case 1:
                if (numAlunos < MAX_ALUNOS) {
                    cout << "\nCadastro do aluno " << numAlunos + 1 << endl;
                    cout << "Nome: ";
                    cin >> alunos[numAlunos].nome;
                    cout << "Idade: ";
                    cin >> alunos[numAlunos].idade;

                    // Solicitar e verificar as notas
                    for (int i = 0; i < NUM_NOTAS; i++) {
                        do {
                            cout << "Nota " << i + 1 << ": ";
                            cin >> alunos[numAlunos].notas[i];
                            if (!verificarNota(alunos[numAlunos].notas[i])) {
                                cout << "Nota fora do intervalo permitido (0 a 10). Tente novamente." << endl;
                            }
                        } while (!verificarNota(alunos[numAlunos].notas[i]));
                    }

                    numAlunos++;
                } else {
                    cout << "\nLimite de alunos atingido!" << endl;
                }
                break;
            case 2:
                cout << "\nListagem de alunos cadastrados:" << endl;
                for (int i = 0; i < numAlunos; i++) {
                    cout << "Aluno " << i + 1 << ":" << endl;
                    cout << "Nome: " << alunos[i].nome << endl;
                    cout << "Idade: " << alunos[i].idade << endl;
                    cout << "Notas: ";
                    for (int j = 0; j < NUM_NOTAS; j++) {
                        cout << alunos[i].notas[j] << " ";
                    }
                    cout << endl;
                }
                break;
            case 3:
                cout << "\nSaindo..." << endl;
                break;
            default:
                cout << "\nOpcao invalida! Tente novamente." << endl;
        }
    } while (opcao != 3);

    return 0;
}


ATIVIDADE 02

#include <iostream>
#include <string>

using namespace std;

const int MAX_ALUNOS = 5;
const int NUM_NOTAS = 4;

// Definição da estrutura Aluno
struct Aluno {
    string nome;
    int idade;
    float notas[NUM_NOTAS];
};

// Função para verificar se uma nota está no intervalo válido (0 a 10)
bool verificarNota(float nota) {
    return (nota >= 0 && nota <= 10);
}

int main() {
    Aluno alunos[MAX_ALUNOS];
    int numAlunos = 0;
    int opcao;

    do {
        cout << "\nSelecione uma opcao:\n";
        cout << "1. Cadastrar novo aluno\n";
        cout << "2. Listar alunos cadastrados\n";
        cout << "3. Sair\n";
        cout << "Opcao: ";
        cin >> opcao;

        switch (opcao) {
            case 1:
                if (numAlunos < MAX_ALUNOS) {
                    cout << "\nCadastro do aluno " << numAlunos + 1 << endl;
                    cout << "Nome: ";
                    cin >> alunos[numAlunos].nome;
                    cout << "Idade: ";
                    cin >> alunos[numAlunos].idade;

                    // Solicitar e verificar as notas
                    for (int i = 0; i < NUM_NOTAS; i++) {
                        do {
                            cout << "Nota " << i + 1 << ": ";
                            cin >> alunos[numAlunos].notas[i];
                            if (!verificarNota(alunos[numAlunos].notas[i])) {
                                cout << "Nota fora do intervalo permitido (0 a 10). Tente novamente." << endl;
                            }
                        } while (!verificarNota(alunos[numAlunos].notas[i]));
                    }

                    numAlunos++;
                } else {
                    cout << "\nLimite de alunos atingido!" << endl;
                }
                break;
            case 2:
                cout << "\nListagem de alunos cadastrados:" << endl;
                for (int i = 0; i < numAlunos; i++) {
                    cout << "Aluno " << i + 1 << ":" << endl;
                    cout << "Nome: " << alunos[i].nome << endl;
                    cout << "Idade: " << alunos[i].idade << endl;
                    cout << "Notas: ";
                    for (int j = 0; j < NUM_NOTAS; j++) {
                        cout << alunos[i].notas[j] << " ";
                    }
                    cout << endl;
                }
                break;
            case 3:
                cout << "\nSaindo..." << endl;
                break;
            default:
                cout << "\nOpcao invalida! Tente novamente." << endl;
        }
    } while (opcao != 3);

    return 0;
}


ATIVIDADE 03

#include <iostream>
#include <string>

using namespace std;

const int MAX_ALUNOS = 5;
const int NUM_NOTAS = 4;

// Definição da estrutura Aluno
struct Aluno {
    string nome;
    int idade;
    float notas[NUM_NOTAS];
    float notaTotal;
    float media;
};

// Função para verificar se uma nota está no intervalo válido (0 a 10)
bool verificarNota(float nota) {
    return (nota >= 0 && nota <= 10);
}

int main() {
    Aluno alunos[MAX_ALUNOS];
    int numAlunos = 0;
    int opcao;

    do {
        cout << "\nSelecione uma opcao:\n";
        cout << "1. Cadastrar novo aluno\n";
        cout << "2. Listar alunos cadastrados\n";
        cout << "3. Sair\n";
        cout << "Opcao: ";
        cin >> opcao;

        switch (opcao) {
            case 1:
                if (numAlunos < MAX_ALUNOS) {
                    cout << "\nCadastro do aluno " << numAlunos + 1 << endl;
                    cout << "Nome: ";
                    cin >> alunos[numAlunos].nome;
                    cout << "Idade: ";
                    cin >> alunos[numAlunos].idade;

                    // Solicitar e verificar as notas
                    float notaTotal = 0;
                    for (int i = 0; i < NUM_NOTAS; i++) {
                        do {
                            cout << "Nota " << i + 1 << ": ";
                            cin >> alunos[numAlunos].notas[i];
                            if (!verificarNota(alunos[numAlunos].notas[i])) {
                                cout << "Nota fora do intervalo permitido (0 a 10). Tente novamente." << endl;
                            }
                        } while (!verificarNota(alunos[numAlunos].notas[i]));
                        notaTotal += alunos[numAlunos].notas[i];
                    }
                    alunos[numAlunos].notaTotal = notaTotal;
                    alunos[numAlunos].media = notaTotal / NUM_NOTAS;

                    numAlunos++;
                } else {
                    cout << "\nLimite de alunos atingido!" << endl;
                }
                break;
            case 2:
                cout << "\nListagem de alunos cadastrados:" << endl;
                for (int i = 0; i < numAlunos; i++) {
                    cout << "Aluno " << i + 1 << ":" << endl;
                    cout << "Nome: " << alunos[i].nome << endl;
                    cout << "Idade: " << alunos[i].idade << endl;
                    cout << "Notas: ";
                    for (int j = 0; j < NUM_NOTAS; j++) {
                        cout << alunos[i].notas[j] << " ";
                    }
                    cout << endl;
                    cout << "Nota Total: " << alunos[i].notaTotal << endl;
                    cout << "Media: " << alunos[i].media << endl;
                }
                break;
            case 3:
                cout << "\nSaindo..." << endl;
                break;
            default:
                cout << "\nOpcao invalida! Tente novamente." << endl;
        }
    } while (opcao != 3);

    return 0;
}


ATIVIDADE 04

#include <iostream>
#include <string>

using namespace std;

const int MAX_ALUNOS = 5;
const int NUM_NOTAS = 4;

// Definição da estrutura Aluno
struct Aluno {
    string nome;
    int idade;
    float notas[NUM_NOTAS];
    float notaTotal;
    float media;
    string resultado;
};

// Função para verificar se uma nota está no intervalo válido (0 a 10)
bool verificarNota(float nota) {
    return (nota >= 0 && nota <= 10);
}

// Função para determinar o resultado com base na média
string determinarResultado(float media) {
    if (media < 4)
        return "Reprovado";
    else if (media >= 4 && media < 6)
        return "Recuperacao";
    else
        return "Aprovado";
}

int main() {
    Aluno alunos[MAX_ALUNOS];
    int numAlunos = 0;
    int opcao;

    do {
        cout << "\nSelecione uma opcao:\n";
        cout << "1. Cadastrar novo aluno\n";
        cout << "2. Listar alunos cadastrados\n";
        cout << "3. Resultado geral dos alunos\n";
        cout << "4. Sair\n";
        cout << "Opcao: ";
        cin >> opcao;

        switch (opcao) {
            case 1:
                if (numAlunos < MAX_ALUNOS) {
                    cout << "\nCadastro do aluno " << numAlunos + 1 << endl;
                    cout << "Nome: ";
                    cin >> alunos[numAlunos].nome;
                    cout << "Idade: ";
                    cin >> alunos[numAlunos].idade;

                    // Solicitar e verificar as notas
                    float notaTotal = 0;
                    for (int i = 0; i < NUM_NOTAS; i++) {
                        do {
                            cout << "Nota " << i + 1 << ": ";
                            cin >> alunos[numAlunos].notas[i];
                            if (!verificarNota(alunos[numAlunos].notas[i])) {
                                cout << "Nota fora do intervalo permitido (0 a 10). Tente novamente." << endl;
                            }
                        } while (!verificarNota(alunos[numAlunos].notas[i]));
                        notaTotal += alunos[numAlunos].notas[i];
                    }
                    alunos[numAlunos].notaTotal = notaTotal;
                    alunos[numAlunos].media = notaTotal / NUM_NOTAS;
                    alunos[numAlunos].resultado = determinarResultado(alunos[numAlunos].media);

                    numAlunos++;
                } else {
                    cout << "\nLimite de alunos atingido!" << endl;
                }
                break;
            case 2:
                cout << "\nListagem de alunos cadastrados:" << endl;
                for (int i = 0; i < numAlunos; i++) {
                    cout << "Aluno " << i + 1 << ":" << endl;
                    cout << "Nome: " << alunos[i].nome << endl;
                    cout << "Idade: " << alunos[i].idade << endl;
                    cout << "Notas: ";
                    for (int j = 0; j < NUM_NOTAS; j++) {
                        cout << alunos[i].notas[j] << " ";
                    }
                    cout << endl;
                    cout << "Nota Total: " << alunos[i].notaTotal << endl;
                    cout << "Media: " << alunos[i].media << endl;
                    cout << "Resultado: " << alunos[i].resultado << endl;
                }
                break;
            case 3:
                cout << "\nResultado geral dos alunos:" << endl;
                for (int i = 0; i < numAlunos; i++) {
                    cout << "Aluno " << i + 1 << ": " << alunos[i].resultado << endl;
                }
                break;
            case 4:
                cout << "\nSaindo..." << endl;
                break;
            default:
                cout << "\nOpcao invalida! Tente novamente." << endl;
        }
    } while (opcao != 4);

    return 0;
}


ATIVIDADE 05

#include <iostream>
#include <string>

using namespace std;

const int MAX_ALUNOS = 5;
const int NUM_NOTAS = 4;

// Definição da estrutura Aluno
struct Aluno {
    string nome;
    int idade;
    float notas[NUM_NOTAS];
    float notaTotal;
    float media;
    string resultado;
};

// Função para verificar se uma nota está no intervalo válido (0 a 10)
bool verificarNota(float nota) {
    return (nota >= 0 && nota <= 10);
}

// Função para determinar o resultado com base na média
string determinarResultado(float media) {
    if (media < 4)
        return "Reprovado";
    else if (media >= 4 && media < 6)
        return "Recuperacao";
    else
        return "Aprovado";
}

int main() {
    Aluno alunos[MAX_ALUNOS];
    int numAlunos = 0;
    int opcao;

    do {
        cout << "\nSelecione uma opcao:\n";
        cout << "1. Cadastrar novo aluno\n";
        cout << "2. Listar alunos cadastrados\n";
        cout << "3. Editar resultado de aluno\n";
        cout << "4. Resultado geral dos alunos\n";
        cout << "5. Sair\n";
        cout << "Opcao: ";
        cin >> opcao;

        switch (opcao) {
            case 1:
                if (numAlunos < MAX_ALUNOS) {
                    cout << "\nCadastro do aluno " << numAlunos + 1 << endl;
                    cout << "Nome: ";
                    cin >> alunos[numAlunos].nome;
                    cout << "Idade: ";
                    cin >> alunos[numAlunos].idade;

                    // Solicitar e verificar as notas
                    float notaTotal = 0;
                    for (int i = 0; i < NUM_NOTAS; i++) {
                        do {
                            cout << "Nota " << i + 1 << ": ";
                            cin >> alunos[numAlunos].notas[i];
                            if (!verificarNota(alunos[numAlunos].notas[i])) {
                                cout << "Nota fora do intervalo permitido (0 a 10). Tente novamente." << endl;
                            }
                        } while (!verificarNota(alunos[numAlunos].notas[i]));
                        notaTotal += alunos[numAlunos].notas[i];
                    }
                    alunos[numAlunos].notaTotal = notaTotal;
                    alunos[numAlunos].media = notaTotal / NUM_NOTAS;
                    alunos[numAlunos].resultado = determinarResultado(alunos[numAlunos].media);

                    numAlunos++;
                } else {
                    cout << "\nLimite de alunos atingido!" << endl;
                }
                break;
            case 2:
                cout << "\nListagem de alunos cadastrados:" << endl;
                for (int i = 0; i < numAlunos; i++) {
                    cout << "Aluno " << i + 1 << ":" << endl;
                    cout << "Nome: " << alunos[i].nome << endl;
                    cout << "Idade: " << alunos[i].idade << endl;
                    cout << "Notas: ";
                    for (int j = 0; j < NUM_NOTAS; j++) {
                        cout << alunos[i].notas[j] << " ";
                    }
                    cout << endl;
                    cout << "Nota Total: " << alunos[i].notaTotal << endl;
                    cout << "Media: " << alunos[i].media << endl;
                    cout << "Resultado: " << alunos[i].resultado << endl;
                }
                break;
            case 3:
                int alunoIndex;
                cout << "\nDigite o numero do aluno que deseja editar: ";
                cin >> alunoIndex;
                alunoIndex--; // Para corresponder ao índice do vetor
                if (alunoIndex >= 0 && alunoIndex < numAlunos) {
                    cout << "Novo resultado (Reprovado/Recuperacao/Aprovado): ";
                    cin >> alunos[alunoIndex].resultado;
                } else {
                    cout << "Aluno nao encontrado!" << endl;
                }
                break;
            case 4:
                cout << "\nResultado geral dos alunos:" << endl;
                for (int i = 0; i < numAlunos; i++) {
                    cout << "Aluno " << i + 1 << ": " << alunos[i].resultado << endl;
                }
                break;
            case 5:
                cout << "\nSaindo..." << endl;
                break;
            default:
                cout << "\nOpcao invalida! Tente novamente." << endl;
        }
    } while (opcao != 5);

    return 0;
}
