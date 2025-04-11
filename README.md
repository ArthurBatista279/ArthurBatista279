 <h1 align="center">
  <a href="#">
    <span class="typed">Arthur, desenvolvedor indie de jogos</span>
  </a>
</h1>


🎮 Apaixonado por jogos 

🛠️ Explorando o mundo da programação, Roblox Studio e desenvolvimento de jogos  

🚀 Em constante evolução: aprendendo, criando e compartilhando


## 💡 Atualmente:
- Criando meu primeiro projeto no Roblox Studio 
- Aprendendo mais sobre modelagem 3D no Blender e integração com Roblox

 ![Arthur GitHub stats](https://github-readme-stats.vercel.app/api?username=ArthurBatista279&theme=dark&show_icons=true)

## 📫 Conecte-se comigo:
 
<div>
<a href = "mailto:contato@barthur.oliveira07@gmail.com"><img loading="lazy" src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white" target="_blank"></a>
<a href="https://www.youtube.com/@Arthurbr-YT" target="_blank"><img loading="lazy" src="https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white" target="_blank"></a>
<a href="https://www.twitch.tv/arthurbryt_oficial" target="_blank"><img loading="lazy" src="https://img.shields.io/badge/Twitch-9146FF?style=for-the-badge&logo=twitch&logoColor=white" target="_blank"></a>
<a href="https://www.linkedin.com/in/arthur-batista-oliveira-bb8018358/" target="_blank"><img loading="lazy" src="https://img.shields.io/badge/-LinkedIn-%230077B5?style=for-the-badge&logo=linkedin&logoColor=white" target="_blank"></a>   
</div>

<!DOCTYPE html>
<html>
<cabeça>
	<meta conjunto de caracteres=utf-8 />
	<title>Contador de Visitas</title>

</cabeçalho>
<corpo>

<?php

	função  get_num_visitas (){
		//conectar
		$ link = mysql_connect ( ' localhost ' , ' root ' , '' );
		se (! $ link ) {
			die ( ' Não foi possível conectar: ​​' . mysql_error ());
		}
		
		mysql_select_db ( " contador " );
		$ query = " SELECIONE total " .
				 " DE `visitas` " .
				 " ORDEM POR total ASC LIMITE 1 " ;
		$ resultado = mysql_query ( $ consulta );
		se (! $ resultado ) {
			$ message   = ' Consulta inválida: ' . mysql_error () . "\n" ;
			$ message .= ' Consulta inteira: ' . $ query ;
			morrer ( $ mensagem );
		}
		se ( mysql_num_rows ( $ resultado ) == 0 ) {
			eco  " Nenhuma linha encontrada, nada para imprimir, então estou saindo " ;
			saída ;
		}
		$ linha = mysql_fetch_array ( $ resultado );
		mysql_close ( $ link );
		retornar  $ linha [ " total " ];
		//fazer consulta
		//retornar total
	}

	function  imprime_visitas ( $ contador ){
		retorne  " <h1> " . $ contador . " </h1> " ;
	}
	
	função  contar_visita (){
		//conectar
		$ link = mysql_connect ( ' localhost ' , ' root ' , '' );
		se (! $ link ) {
			die ( ' Não foi possível conectar: ​​' . mysql_error ());
		}
		
		mysql_select_db ( " contador " );
		$ query = " UPDATE `visitas` " .
				 " DEFINIR total = total + 1 " ;
		$ resultado = mysql_query ( $ consulta );
		se (! $ resultado ) {
			$ message   = ' Consulta inválida: ' . mysql_error () . "\n" ;
			$ message .= ' Consulta inteira: ' . $ query ;
			morrer ( $ mensagem );
		}
		mysql_close ( $ link );
	}

	contar_visita ();
	$ contador = get_num_visitas ();
	echo  imprime_visitas ( $ contador );

?>

 
</corpo>
</html>
