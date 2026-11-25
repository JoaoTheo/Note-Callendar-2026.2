# 1. Histórias de Usuário

<p align="justify">A <i>Tabela 3</i> a seguir contém as Histórias de Usuário (HU) elicitadas para o sistema Note Callendar. Cada história segue o formato <b>"Eu, como [persona], quero [ação], para [benefício]"</b> e possui critérios de aceitação verificáveis, prioridade, rastreabilidade com os Requisitos Funcionais (<a href="RF.md">RF</a>) e Não Funcionais (<a href="RNF.md">RNF</a>) e estimativa em Story Points.</p>

<table>
    <thead>
        <tr>
            <th align="center">ID</th>
            <th align="center">História de Usuário</th>
            <th align="center">Critérios de Aceitação</th>
            <th align="center">Prioridade</th>
            <th align="center">RF/RNF Relacionado</th>
            <th align="center">Story Points</th>
        </tr>
    </thead>
    <tbody>
        <tr id="us01">
            <td align="center">US01</td>
            <td align="justify">Eu, como usuário, quero fazer login na minha conta com e-mail e senha, para acessar e gerenciar minha agenda de forma segura.</td>
            <td align="justify"><ol>
                <li>O sistema deve exibir uma tela de login com os campos de e-mail e senha.</li>
                <li>O sistema deve impedir o envio do formulário com campos vazios ou e-mail em formato inválido.</li>
                <li>Com credenciais válidas, o usuário deve ser redirecionado para a tela principal da agenda.</li>
                <li>Com credenciais inválidas, o sistema deve exibir uma mensagem de erro genérica, sem informar qual dos campos está incorreto.</li>
                <li>A senha deve ser exibida mascarada no campo e transmitida/armazenada de forma segura (nunca em texto puro).</li>
            </ol></td>
            <td align="center">Alta</td>
            <td align="center">RF01<br>RNF04</td>
            <td align="center">8</td>
        </tr>
        <tr id="us02">
            <td align="center">US02</td>
            <td align="justify">Eu, como usuário, quero cadastrar tarefas e compromissos na agenda, para registrar todas as minhas demandas e não esquecer nenhuma delas.</td>
            <td align="justify"><ol>
                <li>A tela principal deve possuir um botão visível para criar um novo evento.</li>
                <li>O formulário deve conter os campos título, data, horário (início e fim) e categoria da atividade.</li>
                <li>Os campos título, data e categoria devem ser obrigatórios; o sistema deve indicar os campos não preenchidos.</li>
                <li>O sistema não deve aceitar um horário de término anterior ao horário de início.</li>
                <li>A criação de um evento deve ser concluída em até 3 interações a partir da tela principal.</li>
                <li>Após salvar, o evento deve aparecer imediatamente na visualização correspondente da agenda.</li>
            </ol></td>
            <td align="center">Alta</td>
            <td align="center">RF02<br>RNF01</td>
            <td align="center">5</td>
        </tr>
        <tr id="us03">
            <td align="center">US03</td>
            <td align="justify">Eu, como usuário, quero alternar a visualização da agenda entre diária, semanal e mensal, para planejar e acompanhar meus compromissos no nível de detalhe que eu precisar.</td>
            <td align="justify"><ol>
                <li>A agenda deve disponibilizar opções para alternar entre as visualizações diária, semanal e mensal.</li>
                <li>A visualização diária deve exibir os eventos do dia selecionado organizados por horário.</li>
                <li>As visualizações semanal e mensal devem exibir um panorama dos eventos de cada dia do período.</li>
                <li>O usuário deve conseguir navegar para o período anterior e o próximo, e retornar à data atual.</li>
                <li>A visualização deve carregar em até 2 segundos em condições normais de uso.</li>
                <li>A interface deve se adaptar a telas de computador e de celular.</li>
            </ol></td>
            <td align="center">Alta</td>
            <td align="center">RF05<br>RNF02<br>RNF03</td>
            <td align="center">8</td>
        </tr>
        <tr id="us04">
            <td align="center">US04</td>
            <td align="justify">Eu, como usuário, quero editar eventos já cadastrados, para manter minha agenda atualizada quando houver mudanças.</td>
            <td align="justify"><ol>
                <li>Ao selecionar um evento na agenda, o sistema deve exibir seus detalhes e a opção de editar.</li>
                <li>O formulário de edição deve vir preenchido com os dados atuais do evento.</li>
                <li>O usuário deve poder alterar título, data, horário, categoria e cor.</li>
                <li>As mesmas validações do cadastro (US02) devem ser aplicadas na edição.</li>
                <li>Após salvar, as alterações devem ser refletidas imediatamente em todas as visualizações.</li>
                <li>Ao cancelar a edição, nenhuma alteração deve ser salva.</li>
            </ol></td>
            <td align="center">Média</td>
            <td align="center">RF06</td>
            <td align="center">3</td>
        </tr>
        <tr id="us05">
            <td align="center">US05</td>
            <td align="justify">Eu, como usuário, quero excluir eventos da agenda, para remover compromissos cancelados ou cadastrados por engano.</td>
            <td align="justify"><ol>
                <li>Ao selecionar um evento, o sistema deve exibir a opção de excluí-lo.</li>
                <li>O sistema deve solicitar confirmação antes de excluir o evento.</li>
                <li>Após a confirmação, o evento deve ser removido de todas as visualizações e deixar de ser contabilizado no indicador de carga e nos relatórios.</li>
                <li>Ao cancelar a confirmação, o evento deve permanecer inalterado.</li>
            </ol></td>
            <td align="center">Média</td>
            <td align="center">RF06</td>
            <td align="center">2</td>
        </tr>
        <tr id="us06">
            <td align="center">US06</td>
            <td align="justify">Eu, como usuário, quero personalizar as cores dos meus eventos e categorias, para identificar rapidamente os diferentes tipos de atividade na agenda.</td>
            <td align="justify"><ol>
                <li>Cada categoria deve possuir uma cor padrão atribuída automaticamente pelo sistema.</li>
                <li>O usuário deve poder escolher uma cor diferente para um evento ou categoria a partir de uma paleta pré-definida.</li>
                <li>A cor escolhida deve ser aplicada imediatamente em todas as visualizações (diária, semanal e mensal).</li>
                <li>As cores da paleta devem garantir contraste suficiente com o texto do evento, mantendo a legibilidade em todas as resoluções.</li>
            </ol></td>
            <td align="center">Média</td>
            <td align="center">RF04<br>RNF05</td>
            <td align="center">3</td>
        </tr>
        <tr id="us07">
            <td align="center">US07</td>
            <td align="justify">Eu, como usuário, quero visualizar um indicador da carga das minhas atividades, para identificar momentos de sobrecarga e redistribuir melhor o meu tempo.</td>
            <td align="justify"><ol>
                <li>O sistema deve calcular o total de horas alocadas em cada dia com base nos horários dos eventos.</li>
                <li>A agenda deve exibir um indicador visual (ex.: barra ou cor de fundo) do nível de carga de cada dia: leve, moderada ou sobrecarregada.</li>
                <li>Dias cuja carga ultrapasse o limite definido (padrão de 8 horas) devem ser destacados como sobrecarregados.</li>
                <li>O indicador deve ser atualizado automaticamente ao criar, editar ou excluir eventos.</li>
            </ol></td>
            <td align="center">Média</td>
            <td align="center">RF03<br>RNF02</td>
            <td align="center">5</td>
        </tr>
        <tr id="us08">
            <td align="center">US08</td>
            <td align="justify">Eu, como usuário, quero gerar relatórios do tempo gasto por categoria de atividade, para entender onde estou investindo meu tempo e acompanhar minha produtividade.</td>
            <td align="justify"><ol>
                <li>O sistema deve oferecer uma seção de relatórios acessível a partir do menu principal.</li>
                <li>O usuário deve poder selecionar o período do relatório (semana, mês ou intervalo personalizado).</li>
                <li>O relatório deve exibir o total de horas e a porcentagem do tempo gasto em cada categoria.</li>
                <li>Os dados devem ser apresentados em gráfico (ex.: pizza ou barras) usando as cores de cada categoria.</li>
                <li>O sistema deve destacar as categorias de atividade mais executadas no período.</li>
                <li>Caso não existam eventos no período, o sistema deve exibir uma mensagem informativa.</li>
            </ol></td>
            <td align="center">Média</td>
            <td align="center">RF07<br>RNF02</td>
            <td align="center">8</td>
        </tr>
    </tbody>
</table>

<div align="center">
<p>Tabela 3: Histórias de Usuário</p>
</div>

# 2. Estimativa

<p align="justify">As histórias foram estimadas em <b>Story Points</b> utilizando a sequência de Fibonacci (1, 2, 3, 5, 8, 13), considerando a complexidade, o esforço e a incerteza de cada uma em relação às demais. A história de exclusão de eventos (US05), por ser a mais simples, foi adotada como referência (2 pontos).</p>

| Prioridade | Histórias              | Total de Story Points |
| :--------: | :--------------------: | :-------------------: |
|    Alta    | US01, US02, US03       |          21           |
|   Média    | US04, US05, US06, US07, US08 |     21          |
| **Total**  | **8 histórias**        |        **42**         |

<div align="center">
<p>Tabela 4: Resumo das estimativas</p>
</div>

# 3. Rastreabilidade

<p align="justify">A <i>Tabela 5</i> relaciona cada requisito às histórias de usuário que o atendem.</p>

| Requisito | Histórias de Usuário |
| :-------: | :------------------: |
|   RF01    |         US01         |
|   RF02    |         US02         |
|   RF03    |         US07         |
|   RF04    |         US06         |
|   RF05    |         US03         |
|   RF06    |      US04, US05      |
|   RF07    |         US08         |
|   RNF01   |         US02         |
|   RNF02   |   US03, US07, US08   |
|   RNF03   |         US03         |
|   RNF04   |         US01         |
|   RNF05   |         US06         |

<div align="center">
<p>Tabela 5: Matriz de rastreabilidade</p>
</div>

# 4. Referências


<a href="../README.md">VOLTAR INÍCIO</a>
