# Day-15

import java.util.ArrayList;

import javax.swing.JOptionPane;

public class CardDriver {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		
		 ArrayList<Card> hand1 = new ArrayList<Card>(7);
		 ArrayList<Card> hand2 = new ArrayList<Card>(7);
		 
		// String cardString;
		 //int cardRequest;
		 int player1Score = 0;
		 int player2Score = 0;

		 DeckOfCards gameDeck = new DeckOfCards();

		 Card card1 = new Card();
		 Card card2 = new Card();

		 gameDeck.shuffle();

		 for ( int x = 0; x < 7; x++)
		  {
		       card1 = gameDeck.deal();
		       hand1.add(card1);

		       card2 = gameDeck.deal();
		       hand2.add(card2);
		   
		  }
		 
		 System.out.println("Player 1's Hand: ");
		 System.out.println("");
		 System.out.println(hand1);

		 System.out.println("");

		 System.out.println("Player 2's Hand: ");
		 System.out.println("");  
		 System.out.println(hand2);
		 
		 for(int counter = 0; counter < hand1.size(); counter++) {
			 for(int revCount = 0; revCount < hand1.size(); revCount++){
			    if(hand1.get(revCount).getFace() == hand1.get(counter).getFace() ) {
			    	  
			    	  hand1.remove(revCount);
			    	  hand1.remove(counter);
			          player1Score++;
			          counter++;
			          revCount++;
			      }
			  }
			 
		 for(int counterTwo = 0; counter < hand2.size(); counterTwo++) {
			 for(int revCount = 0; revCount < hand2.size(); revCount++)
				    if(hand2.get(revCount).getFace() == hand2.get(counterTwo).getFace() ) {
				    	  
				    	  hand2.remove(revCount);
				          hand2.remove(counter);
				          player2Score++;
				          counterTwo++;
				          revCount++;
				      }
				  }
			 
		 
		 System.out.println("");
		 System.out.println("Player 1\'s Score: " + player1Score);
		 
		 System.out.println("");
		 System.out.println("Player 2\'s Score: " + player2Score);
		 
		 System.out.println("---------------");
		 
		 System.out.println("Player 1's Hand: ");
		 System.out.println("");
		 System.out.println(hand1);

		 System.out.println("");

		 System.out.println("Player 2's Hand: ");
		 System.out.println("");  
		 System.out.println(hand2);
		 
		 /* 
		 

		 cardString = JOptionPane.showInputDialog("Player 1: What card will you ask for? (Enter the card's index)");
		 cardRequest = Integer.parseInt(cardString); 
		
		for(int counter = 0; counter < hand1.size(); counter++) {
			    if(hand1.get(cardRequest).getFace() == hand2.get(counter).getFace() ) {
			    	  
			    	  hand1.remove(cardRequest);
			    	  hand2.remove(counter);
			          player1Score++;
			      }
			  } 
		 
		
		 
		 System.out.println("-----Check------");
		 
		 System.out.println("Player 1's Hand: ");
		 System.out.println("");
		 System.out.println(hand1);

		 System.out.println("");

		 System.out.println("Player 2's Hand: ");
		 System.out.println("");
		 System.out.println(hand2);
	
		 */
			   
	}
	
	}}
	

