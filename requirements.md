GebäudeReadModel hat   
  -> Gebäude    
  -> Etagen     
  -> Melder    

  -> Basis für AuftagsCommandModel    
	   -> Command Auftrag für Gebäude    

PrüferPrüflisteReadModel hat    
  -> PrüfAufträge für    
    -> Prüfer "X" und    
    -> Gebäude / Etagen / Melder    

PrüferCommandModel    
	-> Prüfung durchführen für Gebäude / Etage / Melder -> Event Prüfung durchgeführt -> Payload Messwert    
    transformiert nach    
    -> PrüfListenReadModel hat    
		  -> Prüfauftrag / Prüfer / Melder mit Messwert    

	-> Prüfung für Gebäude / Etage abschließen -> Event Prüfung abgeschlossen    

AuftragsCommandModel    
	-> Rechnung erstellen    
		 - vorher optional Event GewünschtePrüfErgebnisseAufBasisDesPrüfersGeändert    
       -> Daten des gewünschten Prüfers für Rechnung heranziehen statt die des bisher eingetragenen Prüfers    
		 -> Event Rechnung erstellt
		
		
	
