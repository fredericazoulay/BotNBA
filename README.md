# BotNBA
Script pour automatiser l'achat de billet de NBA sur le site :
https://www.accorhotelsarena.com/fr/sports-a-Paris/nba-paris-game-2020-presented-bein-sports  

function changeComboBox(inputs, i) {  
    setTimeout(function() {
		inputs.value = 1;
		//var selectedItem = inputs.options[0];
		//var selectedItem = inputs;
		//var selectedText = selectedItem.text;
		//var selectedValue = selectItem.value;
		//selectItem.value = 2;
        //inputs[i].click();
    }, i * 300);
}

function validateCart(btnValidate, i) {  
    setTimeout(function() {
		// controlSelectPlacesCPN1(this);
        //btnValidate[0].click();
		btnValidate.click();
    }, i * 300);
}

function start() {  
	//var inputs = document.getElementsByClassName("nbTickets-691-01-16e023b287d-16e023b287d");
	var inputs = document.getElementById("nbTickets-691-01-16e023b287d-16e023b287d");
	//var inputs_1 = document.getElementsById("nbTickets-691-01-16e023b287d-16e023b287d");
    //var inputs_2 = document.getElementsById("nbTickets-691-02-16e023b287d-16e023b287d");
	//var inputs_3 = document.getElementsById("nbTickets-691-03-16e023b287d-16e023b287d");
	//var inputs_4 = document.getElementsById("nbTickets-691-04-16e023b287d-16e023b287d");
	//var inputs_5 = document.getElementsById("nbTickets-691-05-16e023b287d-16e023b287d");
	//var inputs_6 = document.getElementsById("nbTickets-691-06-16e023b287d-16e023b287d");
	//var inputs_7 = document.getElementsById("nbTickets-691-07-16e023b287d-16e023b287d");
	//var inputs_8 = document.getElementsById("nbTickets-691-08-16e023b287d-16e023b287d");
	//var inputs_9 = document.getElementsById("nbTickets-691-09-16e023b287d-16e023b287d");
	//var inputs_10 = document.getElementsById("nbTickets-691-10-16e023b287d-16e023b287d");
	//var btnValidate = document.getElementById("submitButton");
	var btnValidate = document.getElementById("submitGrilleTarifs");
	//var btnValidate = document.getElementsByClassName("submitGrilleTarifs");
    for(var i = 0; i < inputs.length; i++) {
        changeComboBox(inputs, i);
		validateCart(btnValidate, i);
    }
    setTimeout(function() {
        //var objDiv = document.getElementsByClassName("core-rail")[0];
        //window.scrollTo(0, objDiv.scrollHeight);
        setTimeout(function() {
            start();
        }, 1000);
    }, inputs.length * 300);
}

start();
