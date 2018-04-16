# ip
Práticas Engenharia da Computação - CEFET-MG

Parte 1 (Usando a VM)

git clone https://github.com/tqpessoa/ip.git

cp ~/ip/firewall.py ~/pox/ext/ 

O arquivo firewall.py define as regras do firewall

cp ~/ip/policies ~/pox/pox/misc/ 


Ativando o controlador:

sudo ~/pox/pox.py firewall log.level --DEBUG samples.pretty_log openflow.discovery host_tracker info.packet_dump

Parte 2 (Usando SSH): Utilizando o mininet criar a seguinte topologia:

sudo mn --mac --topo single, 10 --controller=remote, ip=127.0.0.1, port=6633

Cadastrar no arquivo a lista de IPs que não será permitido a comunicação entre eles.

Testar as conexões.

Qual o resultado obtido nos testes de comunicação? Justifique sua resposta.



########################################




Parte 3: Ativando a layer 2 para a tabela arp.

cp ˜/pox/pox/forwarding/l2_learning.py  ˜/pox/ext/

Ativando o controlador:

sudo ~/pox/pox.py l2_learning firewall log.level --DEBUG samples.pretty_log openflow.discovery host_tracker info.packet_dump

Parte 4 (Usando SSH): Utilizando o mininet criar a seguinte topologia:

sudo mn --mac --topo single, 10 --controller=remote, ip=127.0.0.1, port=6633

Cadastrar no arquivo a lista de IPs que não será permitido a comunicação entre eles.

Testar as conexões.
