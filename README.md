 <h1>Hamburguer menu </h1>
 <p>Ícone de alternância de menu usando CSS e Javascript. </p>
 
 <a href="#"><img src="https://user-images.githubusercontent.com/85083611/150660024-407af166-8a1f-461b-b05b-f4a4ebde54a8.gif"   align="center" /> </a>
 
 Ícone projetado em 1990 pelo designer Norm Cox
Um pouco de história
O ícone foi criado em 1980 pelo designer americano Norm Cox para a Xerox Star, a primeira interface gráfica de usuário do mundo.

Existem algumas teorias sobre suas origens, sendo uma delas o símbolo de matemática conhecido como “barra tripla”, que significa equivalência absoluta. Outras explicações são que as “barras” pretendiam se parecer com gavetas de um armário de arquivo.
Após o Xerox Star, o ícone desapareceu por algum tempo.
O que marcou seu retorno? Alguns dizem que a Apple foi o maior motivo para o ressurgimento. O smartphone e a necessidade de uma tela compacta mudaram o jogo. Steve Jobs já era um fã das idéias da Xerox e o resto é história. Saiba mais : [Coletivo UX](https://coletivoux.com/menu-hamburguer-quando-usar-8a53f694a8e9)

~~~css
/*  ===== Resert ===== */

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  background: #021122;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}

/*===== HamburguerMenu =====*/
#toggle {
  position: relative;
  width: 50px;
  height: 50px;
  background: #2cfbc8;
  cursor: pointer;
  display: flex;
  justify-content: center;
  align-items: center;
  transition: 0.2s; 
}

#toggle.active {
  background: #fa3a7a;
}

#toggle::before {
  content: " ";
  position: absolute;
  width: 28px;
  height: 2px;
  background: #ffffff;
  transition: 0.2s;
  transform: translateY(-10px);
  box-shadow: 0 10px 0 #ffffff ;
}

#toggle.active::before {
  transform: translateY(0px) rotate(135deg);
  box-shadow: 0 0 0 #ffffff ;
}

#toggle::after {
  content: '';
  position: absolute;
  width: 28px;
  height: 2px;
  background: #ffffff;
  transition: 0.2s;
  transform: translateY(10px);
}

#toggle.active::after {
  transform: translateY(0px) rotate(-135deg);  
}

~~~

