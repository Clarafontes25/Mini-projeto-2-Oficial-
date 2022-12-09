import java.util.Scanner;

	public class Main {
		
		public static void main(String []args )throws Exception{
			
			Personagem Chapeuzinho = new Personagem();
            Chapeuzinho.nome = "Chapeuzinho";
            Chapeuzinho.energia = 100;

			Personagem Lobo = new Personagem();
            Lobo.nome = "Lobo";
            Lobo.energia = 100;
			
			Scanner leitor = new Scanner (System.in);

			System.out.println("Chapeuzinho! Chapeuzinho!, desça as escadas e leve esses doces para a sua vózinha \n - Cheguei mãe, posso pegar um dos doces? \n - Não! pegue esssa cesta e leve para ela, cuidado ao sair, e vá pelo caminho seguro \n\n Ao sair de casa você se depara com dois caminhos, o caminho seguro demora um pouco mais, contudo o caminho perigoso é mais rápido, qual seguir: \n \n - Caminho seguro \n - Caminho perigoso\n");

			String caminho_bom = "Caminho seguro";

			String caminho = leitor.nextLine();
			
			if(caminho.equals(caminho_bom)){
				Chapeuzinho.alterarEnergia(-75);
				System.out.println("Você foi pelo caminho seguro! Você andou a tarde toda, e chegou cansada na casa de sua avó\n Ao chegar, você foi recebida com um beijo e um abraço quente de sua avó\nVocê teve um final feliz!");
				System.exit(1);
			} else {
				System.out.println("\nAo caminhar na floresta densa, você encontra com um lobo enorme \nvocê se esconde e pensa em no que fazer, ao olhar pro lado você \nVê um coelho e uma pedra muito grande, e você pensa no que jogar para distrair o lobo: \n- Pedra \n- Coelho\n");
			}
				
			String distracao_c = "Coelho";
			String distracao = leitor.nextLine();
				
			if(distracao.equals(distracao_c)) {
				Lobo.alterarEnergia(-25);
				System.out.println("Você joga o coelho e o lobo corre para caça-lo, você anda cuidadosamente, e segue seu caminho\n Após andar um pouco, você vê o lobo novamente e sobre em uma árvore para se esconder");
      } else {
				Chapeuzinho.alterarEnergia(-25);
				System.out.println("Você joga a pedra que é muito pesada para você, já que vocÊ não quer machucar o pobre animal, \ne você corre até uma arvore próxima para se salvar, e o lobo te segue, mas não te vê");
			}
				
			System.out.println("Você olha para baixo e encontra um caminho pelas moitas, contudo, ao longe você percebe espinhos \nVocê deve escolher um caminho: \n- Moita \n- Correr\n");
			
			String correr = "Correr";
			String fuga = leitor.nextLine();
			
			if(fuga.equals(correr)) {
				if(Chapeuzinho.energia >= Lobo.energia){
					System.out.println("Você pula da árvore e corre rapidamente até a casa da sua vó \nao sair da floresta o lobo ainda te persegue, e num ato de desespero o lobo pula em você \nvocê ouve um barulho de tiro, foi um caçador que diz: \n- Cuidado garota, você não pode simplesmente ir pela floresta! \nVocê explica a situação e ele te deixa na casa da sua avó, e ele decide não conta a ela, se você prometer não fazer isso de novo!\nVocê fala que não fará e tem um bom descanso na casa de sua avó");
					System.exit(1);
				} else {
					System.out.println("Você pula da árvore e tenta correr, mas você está cansada e o lobo te pega. \nA sua família espera por sua volta até hoje...");
					System.exit(1);
				}
			} else {
				Chapeuzinho.alterarEnergia(-75);
				System.out.println("Você decide ir pelas moitas e nesse momento, você se sente estranha \nos espinhos eram venenosos e você não consegue fazer mais nada e por isso você desmaia \nUm tempo depois você acorda com um caçador e sua vó ao seu lado, ele diz: \n- Te achei deitada no bosque descordada, você não pode andar por ali! \nSua vó quase chorando diz: \n- Netinha, não faça mais isso, você deixou sua pobre vó preocupada! \nVocê chora e abraça ela, o caçador vai embora e você fica sendo tratada por sua avó!");
			}
		}
	}	
