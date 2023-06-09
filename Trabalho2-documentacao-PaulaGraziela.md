# Trabalho 2: Integração de habilidades - 2023/1
**Disciplina: Redes de Computadores**

**Curso: Engenharia de Computação**

**Nome/RA:** Graziela Militão

**N=41 | NN=29**

**Rede IPV4:** 200.134.41.0/24

**Rede IPV6:** 2001:DB8:CAFE:**29**00::/56

## Tarefa 1:  Sub-Redes
| Sub- Rede |             IPv6 - Sub-Rede            |  IPv4 - Sub-Rede  |  IPv4 - Máscara   | IPv4 - Broadcast  |    
|:---------:|:--------------------------------------:|:-----------------:|:-----------------:|:-----------------:|
| Matriz    | 2001:DB8:CAFE:**29**00::/64 | 200.134.**41**.0   | 255.255.255.192 | 200.134.**41**.**63** |
| Filial 1  | 2001:DB8:CAFE:**29**01::/64 | 200.134.**41**.*64*  | 255.255.255.*224* | 200.134.**41**.*95*  |
| Filial 2  | 2001:DB8:CAFE:**29**02::/64 | 200.134.**41**.*96*  | 255.255.255.*224* | 200.134.**41**.*127* |
| Filial 3  | 2001:DB8:CAFE:**29**03::/64 | 200.134.**41**.*128* | 255.255.255.*224* | 200.134.**41**.*159* |
| Filial 4  | 2001:DB8:CAFE:**29**04::/64 | 200.134.**41**.*160* | 255.255.255.*224* | 200.134.**41**.*191* |
| Filial 5  | 2001:DB8:CAFE:**29**05::/64 | 200.134.**41**.*192* | 255.255.255.*224* | 200.134.**41**.*223* |
| pb-vit    | 2001:DB8:CAFE:**29**FF::00:0/112 | 200.134.**41**.*224* | 255.255.255.*252* | 200.134.**41**.*227* |
| vit-fb    | 2001:DB8:CAFE:**29**FF::01:0/112 | 200.134.**41**.*228* | 255.255.255.*252* | 200.134.**41**.*231* |
| fb-ita    | 2001:DB8:CAFE:**29**FF::02:0/112 | 200.134.**41**.*232* | 255.255.255.*252* | 200.134.**41**.*235* |
| ita-pb    | 2001:DB8:CAFE:**29**FF::03:0/112 | 200.134.**41**.*236* | 255.255.255.*252* | 200.134.**41**.*239* |
| cv-ita    | 2001:DB8:CAFE:**29**FF::04:0/112  | 200.134.**41**.*240* | 255.255.255.*252* | 200.134.**41**.*243* |


## Tarefa 2: Endereçamento de Dispositivos
| Dispositivo           |Interface|      IPv4     |  IPv4 - Máscara |IPv4 - Gateway|      IPv6/Prefixo (GUA)     | IPv6 (LLA) |IPv6-Gateway|
|:-----------------------:|:---------:|---------------|-----------------|--------------|-----------------------------|------------|---------|
| PC1                   | NIC     | 200.134.**41**.*3*   | 255.255.255.*192* | 200.134.**41**.*1*  | 2001:DB8:CAFE:**29***00*::*3*/64    |   EUI-64   | FE80::1 |
| PC2                   | NIC     | 200.134.**41**.*4*   | 255.255.255.*192* | 200.134.**41**.*1*  | 2001:DB8:CAFE:**29***00*::*4*/64    |   EUI-64   | FE80::1 |
| PC3                   | NIC     | 200.134.**41**.*67*   | 255.255.255.*224* | 200.134.**41**.*65*  | 2001:DB8:CAFE:**29***01*::*3*/64    |   EUI-64   | FE80::1 |
| PC4                   | NIC     | 200.134.**41**.*68*  | 255.255.255.*224* | 200.134.**41**.*65* | 2001:DB8:CAFE:**29***01*::*4*/64    |   EUI-64   | FE80::1 |
| PC5                   | NIC     | 200.134.**41**.*99*  | 255.255.255.*224* | 200.134.**41**.*97* | 2001:DB8:CAFE:**29***02*::*3*/64    |   EUI-64   | FE80::1 |
| PC6                   | NIC     | 200.134.**41**.*100* | 255.255.255.*224* | 200.134.**41**.*97* | 2001:DB8:CAFE:**29***02*::*4*/64    |   EUI-64   | FE80::1 |
| Switch-Matriz         | SVI     | 200.134.**41**.*2*   | 255.255.255.*192* | 200.134.**41**.*1*  |             -               |     -      |    -    |
| Switch-Filial1        | SVI     | 200.134.**41**.*66*  | 255.255.255.*224* | 200.134.**41**.*65* |             -               |     -      |    -    |
| Switch-Filial2        | SVI     | 200.134.**41**.*98*  | 255.255.255.*224* | 200.134.**41**.*97* |             -               |     -      |    -    |
| Roteador-Pato Branco  | Fa0/0   | 200.134.**41**.*1*   | 255.255.255.*192* |      -       | 2001:DB8:CAFE:**29** *00*::*1*/64    |   FE80::1  |    -    |
| Roteador-Pato Branco  | Se0/0/0 | 200.134.**41**.*225* | 255.255.255.*252* |      -       | 2001:DB8:CAFE:**29**FF::*00*:*1*/112 |   EUI-64   |    -    |
| Roteador-Pato Branco  | Se0/0/1 | 200.134.**41**.*238* | 255.255.255.*252* |      -       | 2001:DB8:CAFE:**29**FF::*03*:*2*/112 |   EUI-64   |    -    |
| Roteador-Fco. Beltrão | Fa0/0   | 200.134.**41**.*65*  | 255.255.255.*224* |      -       | 2001:DB8:CAFE:**29** *00*::*1*/64    |   FE80::1  |    -    |
| Roteador-Fco. Beltrão | Se0/0/0 | 200.134.**41**.*233* | 255.255.255.*252* |      -       | 2001:DB8:CAFE:**29**FF::*02*:*1*/112 |   EUI-64   |    -    |
| Roteador-Fco. Beltrão | Se0/0/1 | 200.134.**41**.*230* | 255.255.255.*252* |      -       | 2001:DB8:CAFE:**29**FF::*01*:*2*/112 |   EUI-64   |    -    | 
| Roteador-Vitorino     | Se0/0/1 | 200.134.**41**.*226* | 255.255.255.*252* |      -       | 2001:DB8:CAFE:**29**FF::*00*:*2*/112 |   EUI-64   |    -    | 
| Roteador-Vitorino     | Se0/0/0 | 200.134.**41**.*229* | 255.255.255.*252* |      -       | 2001:DB8:CAFE:**29**FF::*01*:*1*/112 |   EUI-64   |    -    | 
| Roteador-Itapejara    | Se0/0/0 | 200.134.**41**.*237* | 255.255.255.*252* |      -       | 2001:DB8:CAFE:**29**FF::*03*:*1*/112 |   EUI-64   |    -    | 
| Roteador-Itapejara    | Se0/0/1 | 200.134.**41**.*234* | 255.255.255.*252* |      -       | 2001:DB8:CAFE:**29**FF::*02*:*2*/112 |   EUI-64   |    -    | 
| Roteador-Itapejara    |  Fa0/1  | 200.134.**41**.*241* | 255.255.255.*252* |      -       | 2001:DB8:CAFE:**29**FF::*04*:*1*/112 |   EUI-64   |    -    | 
| Roteador-Coronel      | Fa0/0   | 200.134.**41**.*97*  | 255.255.255.*224* |      -       | 2001:DB8:CAFE:**29** *02*::*1*/64    |   FE80::1  |    -    |
| Roteador-Coronel      | Fa0/1   | 200.134.**41**.*242* | 255.255.255.*252* |      -       | 2001:DB8:CAFE:**29**FF::*04*:*2*/112 |   EUI-64   |    -    | 



## Tarefa 3: Tabela de Roteamento
#### IPv4

### Roteador Pato Branco
|  Rede de Destino  |     Máscara     |     Next Hop      | Interface de Saída |
|-------------------|-----------------|-------------------|--------------------|
|  200.134.41.240   | 255.255.255.252 |  200.134.41.226   |       Se0/0/0      | 
|  200.134.41.64    | 255.255.255.224 |  200.134.41.226   |       Se0/0/0      | 
|  200.134.41.96    | 255.255.255.224 |  200.134.41.226   |       Se0/0/0      | 
|  200.134.41.228   | 255.255.255.252 |  200.134.41.226   |       Se0/0/0      | 
|  200.134.41.232   | 255.255.255.252 |  200.134.41.226   |       Se0/0/0      | 


#### Roteador Francisco Beltrão
|  Rede de Destino  |     Máscara     |     Next Hop      | Interface de Saída |
|-------------------|-----------------|-------------------|--------------------|
|  200.134.41.240   | 255.255.255.252 |  200.134.41.234   |       Se0/0/0      | 
|  200.134.41.236   | 255.255.255.252 |  200.134.41.234   |       Se0/0/0      | 
|  200.134.41.0     | 255.255.255.192 |  200.134.41.234   |       Se0/0/0      | 
|  200.134.41.96    | 255.255.255.224 |  200.134.41.234   |       Se0/0/0      | 
|  200.134.41.224   | 255.255.255.252 |  200.134.41.234   |       Se0/0/0      | 

#### Roteador Vitorino
|  Rede de Destino  |     Máscara     |     Next Hop      | Interface de Saída |
|-------------------|-----------------|-------------------|--------------------|
|  200.134.41.64    | 255.255.255.224 |  200.134.41.230   |       Se0/0/0      | 
|  200.134.41.232   | 255.255.255.252 |  200.134.41.230   |       Se0/0/0      | 
|  200.134.41.240   | 255.255.255.252 |  200.134.41.230   |       Se0/0/0      | 
|  200.134.41.96    | 255.255.255.224 |  200.134.41.230   |       Se0/0/0      | 
|  200.134.41.236   | 255.255.255.252 |  200.134.41.230   |       Se0/0/0      | 
|  200.134.41.0     | 255.255.255.192 |  200.134.41.230   |       Se0/0/0      | 

#### Roteador Itapejara D'Oeste
|  Rede de Destino  |     Máscara     |     Next Hop      | Interface de Saída |
|-------------------|-----------------|-------------------|--------------------|
|  200.134.41.96    | 255.255.255.224 |  200.134.41.242   |       Fa0/1        | 
|  200.134.41.0     | 255.255.255.192 |  200.134.41.238   |      Se0/0/0       | 
|  200.134.41.64    | 255.255.255.224 |  200.134.41.238   |      Se0/0/0       | 
|  200.134.41.224   | 255.255.255.252 |  200.134.41.238   |      Se0/0/0       | 
|  200.134.41.228   | 255.255.255.252 |  200.134.41.238   |      Se0/0/0       | 

#### Roteador Coronel Vivida
|  Rede de Destino  |     Máscara     |     Next Hop      | Interface de Saída |
|-------------------|-----------------|-------------------|--------------------|
|  200.134.41.236   | 255.255.255.252 |  200.134.41.241   |       Fa0/1        | 
|  200.134.41.0     | 255.255.255.192 |  200.134.41.241   |       Fa0/1        | 
|  200.134.41.224   | 255.255.255.252 |  200.134.41.241   |       Fa0/1        | 
|  200.134.41.228   | 255.255.255.252 |  200.134.41.241   |       Fa0/1        | 
|  200.134.41.64    | 255.255.255.224 |  200.134.41.241   |       Fa0/1        | 
|  200.134.41.232   | 255.255.255.252 |  200.134.41.241   |       Fa0/1        | 

### IPv6
#### Roteador Pato Branco
| Rede de Destino/Prefixo          | Next Hop                       | Interface de Saída        |
|----------------------------------|--------------------------------|---------------------------|
| 2001:DB8:CAFE:**29**FF::04:0/112 |  2001:DB8:CAFE:**29**FF::00:2  |       Se0/0/0             |
| 2001:DB8:CAFE:**29**01::/64      |  2001:DB8:CAFE:**29**FF::00:2  |       Se0/0/0             |
| 2001:DB8:CAFE:**29**02::/64      |  2001:DB8:CAFE:**29**FF::00:2  |       Se0/0/0             |
| 2001:DB8:CAFE:**29**FF::01:0/112 |  2001:DB8:CAFE:**29**FF::00:2  |       Se0/0/0             |
| 2001:DB8:CAFE:**29**FF::02:0/112 |  2001:DB8:CAFE:**29**FF::00:2  |       Se0/0/0             |      
      
#### Roteador Francisco Beltrão
| Rede de Destino/Prefixo          | Next Hop                       | Interface de Saída        |
|----------------------------------|--------------------------------|---------------------------|
| 2001:DB8:CAFE:**29**FF::04:0/112 |  2001:DB8:CAFE:**29**FF::02:2  |       Se0/0/0             |
| 2001:DB8:CAFE:**29**FF::03:0/112 |  2001:DB8:CAFE:**29**FF::02:2  |       Se0/0/0             |
| 2001:DB8:CAFE:**29**00::/64      |  2001:DB8:CAFE:**29**FF::02:2  |       Se0/0/0             |
| 2001:DB8:CAFE:**29**02::/64      |  2001:DB8:CAFE:**29**FF::02:2  |       Se0/0/0             |
| 2001:DB8:CAFE:**29**FF::00:0/112 |  2001:DB8:CAFE:**29**FF::02:2  |       Se0/0/0             |      
       
#### Roteador Vitorino
| Rede de Destino/Prefixo          |  Next Hop                      | Interface de Saída        |
|----------------------------------|--------------------------------|---------------------------|
| 2001:DB8:CAFE:**29**01::/64      |  2001:DB8:CAFE:**29**FF::01:2  |       Se0/0/0             |
| 2001:DB8:CAFE:**29**FF::02:0/112 |  2001:DB8:CAFE:**29**FF::01:2  |       Se0/0/0             |
| 2001:DB8:CAFE:**29**FF::04:0/112 |  2001:DB8:CAFE:**29**FF::01:2  |       Se0/0/0             |
| 2001:DB8:CAFE:**29**02::/64      |  2001:DB8:CAFE:**29**FF::01:2  |        Se0/0/0             |
| 2001:DB8:CAFE:**29**FF::03:0/112 |  2001:DB8:CAFE:**29**FF::01:2  |        Se0/0/0             |    
| 2001:DB8:CAFE:**29**00::/64      |  2001:DB8:CAFE:**29**FF::01:2  |       Se0/0/0             |

#### Roteador Itapejara D'Oeste
| Rede de Destino/Prefixo          | Next Hop                       | Interface de Saída        |
|----------------------------------|--------------------------------|---------------------------|
| 2001:DB8:CAFE:**29**02::/64      |  2001:DB8:CAFE:**29**FF::04:2  |         Fa0/1             |
| 2001:DB8:CAFE:**29**00::/64      |  2001:DB8:CAFE:**29**FF::03:2  |       Se0/0/0             |
| 2001:DB8:CAFE:**29**01::/64      |  2001:DB8:CAFE:**29**FF::03:2  |       Se0/0/0             |
| 2001:DB8:CAFE:**29**FF::00:0/112 |  2001:DB8:CAFE:**29**FF::03:2  |       Se0/0/0             |    
| 2001:DB8:CAFE:**29**FF::01:0/112 |  2001:DB8:CAFE:**29**FF::03:2  |       Se0/0/0             |

#### Roteador Coronel Vivida
| Rede de Destino/Prefixo          | Next Hop                       | Interface de Saída        |
|----------------------------------|--------------------------------|---------------------------|
| 2001:DB8:CAFE:**29**FF::03:0/112 |  2001:DB8:CAFE:**29**FF::04:1  |       Fa0/1               |
| 2001:DB8:CAFE:**29**00::/64      |  2001:DB8:CAFE:**29**FF::04:1  |       Fa0/1               |
| 2001:DB8:CAFE:**29**FF::00:0/112 |  2001:DB8:CAFE:**29**FF::04:1  |       Fa0/1               |
| 2001:DB8:CAFE:**29**FF::01:0/112 |  2001:DB8:CAFE:**29**FF::04:1  |       Fa0/1               |
| 2001:DB8:CAFE:**29**01::/64      |  2001:DB8:CAFE:**29**FF::04:1  |       Fa0/1               |
| 2001:DB8:CAFE:**29**FF::02:0/112 |  2001:DB8:CAFE:**29**FF::04:1  |       Fa0/1               |

## Topologia - Packet Tracer
