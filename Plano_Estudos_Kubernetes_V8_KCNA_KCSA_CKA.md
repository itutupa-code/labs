# Kubernetes Certification Lab

Plano de estudos e laboratórios locais — KCNA, KCSA e CKA

Proposta de capacitação colaborativa para profissionais da V8 | Versão 1.0 | 28 de outubro de 2026

Escopo: certificações CNCF KCNA, KCSA e CKA. Não estão incluídas especializações em plataformas de nuvem ou distribuições empresariais.

## 1. Visão geral

O projeto estabelece uma trilha progressiva para que os participantes estudem conceitos de Kubernetes, executem desafios práticos em clusters individuais e se preparem para as certificações KCNA (fundamentos), KCSA (segurança) e CKA (administração). Cada integrante é responsável por seu próprio laboratório, enquanto roteiros, exercícios e critérios de validação são padronizados para todo o grupo.

## 2. Objetivos e resultados esperados

- Criar autonomia na instalação, operação, diagnóstico e manutenção de clusters Kubernetes.

- Consolidar fundamentos teóricos para a KCNA e segurança cloud native para a KCSA.

- Desenvolver fluência operacional com kubectl, YAML, redes, armazenamento, kubeadm, etcd e troubleshooting para a CKA.

- Disponibilizar um conjunto versionado e reproduzível de laboratórios, scripts, desafios e gabaritos.

- Avaliar a prontidão de cada participante por evidências práticas e simulados, sem depender apenas da presença nas reuniões.

## 3. Trilha e calendário de referência

| Etapa | Duração sugerida | Meta | Entregáveis |
| --- | --- | --- | --- |
| 1 — KCNA | 4 a 6 semanas | Conhecimento de arquitetura e fundamentos | 12 labs; exercícios conceituais; simulado |
| 2 — KCSA | 4 a 6 semanas | Segurança de Kubernetes e ecossistema | 12 labs; checklist de segurança; simulado |
| 3 — CKA | 12 a 16 semanas | Administração operacional e solução de incidentes | 30 labs; cluster kubeadm; simulados cronometrados |

Estimativa total: 20 a 28 semanas, supondo dedicação média de 5 a 7 horas por pessoa a cada semana. O agendamento das provas depende do desempenho individual; os prazos não são garantias de aprovação.

## 4. Arquitetura dos laboratórios locais

Ambiente A — Kind (KCNA, KCSA e início da CKA): cada participante usa Linux nativo ou Windows 11 com WSL2, Docker, Kind e kubectl. Cluster de referência: um control plane e dois workers. O cluster pode ser descartado e reconstruído rapidamente.

Ambiente B — kubeadm (módulo CKA): cluster separado em VMs Linux locais, com um control plane e dois workers quando houver recursos suficientes. Esse ambiente permite praticar instalação, upgrades, kubelet, administração de certificados, recuperação de falhas e etcd.

| Item | Recomendação inicial |
| --- | --- |
| CPU | 4 núcleos ou mais |
| Memória | 16 GB de RAM no computador (ajustar ao perfil das VMs) |
| Disco livre | 40 a 60 GB inicialmente; revisar para kubeadm |
| Sistema | Linux ou Windows 11 com WSL2 |
| Ferramentas | Docker, Kind, kubectl, Helm, Git, editor YAML; posteriormente kubeadm e VMs Linux |

Nota: requisitos sugeridos para estudo; não são requisitos oficiais de exame. Não é necessário um cluster compartilhado. Exercícios com CNI/NetworkPolicy exigem plugin de rede compatível; o Kind padrão pode não aplicar essas políticas sem configuração adicional.

## 5. Método de ensino por laboratório

1. Teoria: apresentar objetivo, conceitos, componentes e pré-requisitos.

2. Demonstração guiada: mostrar um caso comentado, sem substituir a resolução individual.

3. Desafio individual: executar instruções no próprio cluster, com o mínimo de pistas.

4. Validação objetiva: checar estado, conectividade, permissões ou recuperação do serviço.

5. Retrospectiva: comparar soluções, registrar erros comuns e publicar aprendizados.

Modelo de entrega: ID, título, certificação, competências, tempo estimado, pré-requisitos, cenário, tarefa, comandos de validação, evidências esperadas, procedimento de reset e gabarito separado.

## 6. Catálogo inicial de laboratórios

| Lab | Atividade | Trilha |
| --- | --- | --- |
| LAB-001 | Ferramentas, Docker/Kind e cluster local | KCNA |
| LAB-002 | Componentes do control plane e workers | KCNA |
| LAB-003 | Pods: criar, consultar e excluir | KCNA |
| LAB-004 | Deployments e ReplicaSets | KCNA |
| LAB-005 | Escala e rolling updates | KCNA |
| LAB-006 | Services e conectividade | KCNA |
| LAB-007 | Namespaces, ConfigMaps e Secrets | KCNA |
| LAB-008 | Logs, eventos e diagnóstico básico | KCNA |
| LAB-009 | Conceitos de DNS e discovery | KCNA |
| LAB-010 | Volumes e persistência introdutória | KCNA |
| LAB-011 | Scheduling e recursos de containers | KCNA |
| LAB-012 | Revisão e simulado aplicado | KCNA |
| LAB-013 | ServiceAccounts e RBAC | KCSA |
| LAB-014 | Princípio do menor privilégio | KCSA |
| LAB-015 | SecurityContext | KCSA |
| LAB-016 | Pod Security Standards | KCSA |
| LAB-017 | NetworkPolicies (com CNI compatível) | KCSA |
| LAB-018 | Secrets e proteção de dados | KCSA |
| LAB-019 | Supply chain e imagens de containers | KCSA |
| LAB-020 | Scanning e análise de imagens | KCSA |
| LAB-021 | Threat modeling de workloads | KCSA |
| LAB-022 | Hardening de manifestos | KCSA |
| LAB-023 | Auditoria e análise de configurações | KCSA |
| LAB-024 | Revisão e simulado de segurança | KCSA |

| Lab | Atividade | Trilha |
| --- | --- | --- |
| LAB-025 | Preparação das VMs Linux | CKA |
| LAB-026 | Criar cluster com kubeadm | CKA |
| LAB-027 | Inspecionar componentes e certificados | CKA |
| LAB-028 | Administrar e drenar nós | CKA |
| LAB-029 | Taints, tolerations e affinity | CKA |
| LAB-030 | Recursos, probes e scheduling | CKA |
| LAB-031 | Deployments e atualização de workloads | CKA |
| LAB-032 | Jobs, CronJobs e DaemonSets | CKA |
| LAB-033 | Services e troubleshooting de rede | CKA |
| LAB-034 | CoreDNS e resolução de nomes | CKA |
| LAB-035 | NetworkPolicies e CNI | CKA |
| LAB-036 | Ingress/Gateway conforme currículo | CKA |
| LAB-037 | PV, PVC e StorageClass | CKA |
| LAB-038 | Falhas de montagem e persistência | CKA |
| LAB-039 | RBAC e controle de acesso | CKA |
| LAB-040 | Helm e Kustomize | CKA |
| LAB-041 | CRDs e recursos customizados | CKA |
| LAB-042 | Upgrade do cluster via kubeadm | CKA |
| LAB-043 | Backup de etcd | CKA |
| LAB-044 | Restauração de etcd | CKA |
| LAB-045 | Worker em NotReady | CKA |
| LAB-046 | Pod em CrashLoopBackOff | CKA |
| LAB-047 | Pod em Pending | CKA |
| LAB-048 | Falha de service selector / endpoints | CKA |
| LAB-049 | Falha de DNS | CKA |
| LAB-050 | Falha de control plane | CKA |
| LAB-051 | Permissões e autenticação | CKA |
| LAB-052 | Exercícios de performance operacional | CKA |
| LAB-053 | Simulado CKA 1 | CKA |
| LAB-054 | Simulado CKA 2 | CKA |

## 7. Organização semanal e colaboração

- Encontro semanal de 90 minutos: apresentação curta, demonstração e início dos exercícios.

- Atividade individual entre encontros: executar desafios e registrar evidências.

- Rodízio de facilitadores: um integrante prepara cenário e outro revisa validação.

- Revisão semanal ou quinzenal: discutir decisões técnicas, erros e alternativas.

- Simulados: começar com quizzes para KCNA/KCSA; evoluir para tarefas cronometradas na CKA.

## 8. Repositório sugerido

`setup/` — pré-requisitos, instalação e definições dos clusters

`kcna/` — fundamentos, laboratórios e simulados

`kcsa/` — segurança, políticas, cenários e simulados

`cka/` — operações, kubeadm, troubleshooting e simulados

`scripts/` — criação, reset, validação e coleta de evidências

`solucoes/` — gabaritos separados (acesso controlado)

## 9. Prontidão para certificação

| Dimensão | Critério interno sugerido |
| --- | --- |
| Participação | Concluir os laboratórios obrigatórios e explicar o resultado |
| KCNA | Acertar ao menos 80% em simulados de conteúdo |
| KCSA | Acertar ao menos 80% em simulados e justificar decisões de segurança |
| CKA | Resolver tarefas sem gabarito e atingir 80% em dois simulados cronometrados |
| Qualidade | Publicar evidências reproduzíveis, com comandos, YAML e resultado |

Os 80% são metas internas de prontidão, não equivalem à nota oficial de aprovação. Verificar sempre duração, ambiente e domínio de competências publicados pelo organizador antes de agendar uma prova.

## 10. LAB-001 — Criação do cluster local

Objetivo: disponibilizar o primeiro cluster de três nós, validar componentes básicos e demonstrar entendimento da arquitetura.

Pré-requisitos: Docker funcionando, Kind e kubectl instalados; Linux ou WSL2 configurado.

Arquivo: kind-cluster.yaml

```yaml
kind: Cluster
apiVersion: kind.x-k8s.io/v1alpha4
nodes:
- role: control-plane
- role: worker
- role: worker
```

Comandos de execução:

```bash
kind create cluster --name k8s-study --config kind-cluster.yaml --wait 5m
kubectl get nodes -o wide
kubectl get pods -n kube-system
kubectl cluster-info
kubectl config current-context
```

Critérios de aceite: os três nós estão Ready; componentes essenciais em kube-system estão saudáveis; o participante consegue explicar control plane, worker, API Server, Scheduler, Controller Manager, etcd e kubelet.

Reset do ambiente: kind delete cluster --name k8s-study. Antes de criar recursos, confirmar que kubectl está apontando para o contexto correto para evitar alterações em clusters externos.

## 11. Governança e próximos passos

- Definir número de participantes e responsável pela curadoria do conteúdo.

- Verificar disponibilidade de RAM/disco e padronizar SO, versões e ferramentas.

- Criar repositório versionado e modelo de README para laboratórios.

- Executar LAB-001 em todos os computadores e registrar dificuldades.

- Publicar agenda das primeiras quatro semanas da KCNA e configurar exercícios de acompanhamento.

## 12. Referências oficiais

CNCF / Linux Foundation — certificações: https://training.linuxfoundation.org/certification/

Documentação Kubernetes: https://kubernetes.io/docs/

Kind: https://kind.sigs.k8s.io/

kubeadm: https://kubernetes.io/docs/setup/production-environment/tools/kubeadm/

Pod Security Standards: https://kubernetes.io/docs/concepts/security/pod-security-standards/

Nota de manutenção: este documento é um plano de capacitação e deve ser conferido periodicamente com os currículos oficiais, que podem sofrer alterações.


## 13. Início rápido — ambientação da equipe

> **Primeira missão:** todos executarem o LAB-001 localmente, sem alterar clusters de clientes ou ambientes corporativos.

### 13.1 Checklist de instalação

- [ ] Linux nativo ou WSL2 configurado.
- [ ] Docker instalado e daemon acessível (`docker info`).
- [ ] `kind` instalado (`kind version`).
- [ ] `kubectl` instalado (`kubectl version --client`).
- [ ] Git instalado (`git --version`).
- [ ] Editor de texto configurado (VS Code é opcional).

### 13.2 Validar as ferramentas

```bash
docker info
kind version
kubectl version --client
git --version
```

Caso `docker info` falhe, resolver o funcionamento do Docker antes de prosseguir. No Windows com WSL2, conferir a integração do Docker com a distribuição Linux.

### 13.3 Executar o LAB-001

Na pasta do laboratório, crie `kind-cluster.yaml`:

```yaml
kind: Cluster
apiVersion: kind.x-k8s.io/v1alpha4
nodes:
  - role: control-plane
  - role: worker
  - role: worker
```

Execute:

```bash
kind create cluster --name k8s-study --config kind-cluster.yaml --wait 5m
kubectl config use-context kind-k8s-study
kubectl get nodes -o wide
kubectl get pods -A
kubectl cluster-info
```

**Aceite:** 3 nós `Ready`, componentes do sistema saudáveis, contexto `kind-k8s-study` ativo. Não prosseguir com comandos destrutivos sem conferir o contexto atual.

### 13.4 Entrega individual

Registrar no repositório (ou enviar ao grupo):

- Sistema operacional e versões do Docker, Kind e kubectl.
- Saída de `kubectl get nodes -o wide`.
- Breve explicação da diferença entre control plane e worker.
- Dificuldades encontradas e como foram solucionadas.

### 13.5 Perguntas de revisão

1. Qual é a função do API Server?
2. O que o etcd armazena?
3. Qual a responsabilidade do Scheduler?
4. Qual é a diferença entre Pod e Node?
5. O que acontece se um container de um Pod terminar?

### 13.6 Próxima atividade

**LAB-002:** explorar objetos e componentes do cluster com `kubectl get`, `kubectl describe`, `kubectl explain` e consultas ao namespace `kube-system`. O desafio será entregar um mapa descritivo da arquitetura observada no próprio ambiente.

---

*Plano vivo de estudo. Atualizar versões de ferramentas e verificar os conteúdos das provas nos sites oficiais antes de agendar os exames.*
