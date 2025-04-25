### Donde y que colocar los elementos dentro del main.cpp

### Definiciones pre setup

  #include "buzzer/buzzer.h"
  #define BUZZER_PIN 5

### Setup

    buzzerInit(BUZZER_PIN);

### Loop

    if      (cmd == "100") { 
      currentAlarm = A_LOW; 
      Serial.println("Alarma nivel bajo activada"); 
    }
    else if (cmd == "200") { 
      currentAlarm = A_MEDIUM; 
      Serial.println("Alarma nivel medio activada"); 
    }
    else if (cmd == "300") { 
      currentAlarm = A_HIGH; 
      Serial.println("Alarma nivel alto activada"); 
    }
    else { 
      currentAlarm = A_NONE; 
      Serial.println("Alarma desactivada"); 
    }
  buzzerUpdate();