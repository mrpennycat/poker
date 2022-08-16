# pokermport java.util.ArrayList;

public class Deck {

	//Posibles valores de los atributos para construir objetos Card
	private final String[] PALO = {"corazones", "diamantes", "trébol", "picas"};
	private final String[] COLOR = {"rojo", "negro"};
	private final String[] VALOR = { "2", "3", "4", "5", "6", "7", "8", "9", "10", "A", "J", "Q", "K"};

	//Mazo de cartas
	private ArrayList<Card> deck;

	public Deck() {
		deck = new ArrayList<Card>();

		//Construimos cartas de color ROJO
		for (int palo = 0; palo < 2; palo++) //Se usa PALO[0] y PALO[1]
			for (int valor = 0; valor < VALOR.length; valor++)
				deck.add(new Card(PALO[palo], COLOR[0], VALOR[valor]));

		//Construimos cartas de color NEGRO
		for (int palo = 2; palo < 4; palo++) //Se usa PALO[2] y PALO[3]
			for (int valor = 0; valor < VALOR.length; valor++)
				deck.add(new Card(PALO[palo], COLOR[1], VALOR[valor]));
	}
	
	/**
	 * Retorna cuantas cartas tiene este mazo.
	 * El tamaño correcto tras la creación debería ser 52 cartas.
	 * @return Tamaño actual del mazo.
	 */
	public int getSize() {
		return deck.size();
	}

}
