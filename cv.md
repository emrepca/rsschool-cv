# Muhammet Emre Paça

## Junior Frontend Developer

### Contact information:

Phone: +90 5414884253

E-mail: <emrepaca3@gmail.com>

Discord: emrepaca#6536

[Linkedin](https://www.linkedin.com/in/muhammet-emre-pa%C3%A7a/)

### About myself:

I am a 3rd year university student in Turkey. I want to learn *Front-End Development* in **RSSchool!**

I am trying to improve myself in the field of software and I take many online courses for this.

### Skills and Proficiency:

    - HTML5, CSS3 Basic Level

    - C# Intermediate Level

    - C Intermediate Level

    - Git, Github

    - Editors: VS, VS Code, Dev C++

    ### Code examples:

**Craps game** in C language. Using the **rand** and **srand** functions.



```

#include <stdio.h>

#include <stdlib.h>

#include <time.h>

int RollingtheDice (void){

	int dice1,dice2,totaldice;

	dice1=1+(rand()%6);

	dice2=1+(rand()%6);

	totaldice=dice1+dice2;

	printf("Player %d + %d = %d threw.\n",dice1,dice2,totaldice);

	return totaldice;

}



int main (){

	int total;

	int gamestate,playerrating;

	srand(time(NULL));

	total = RollingtheDice();

	switch (total){

		case 7: case 11: gamestate = 1;

		break;

		case 2: case 3: case 12: gamestate = 2;

		break;

		default: gamestate = 0; playerrating = total;

		printf("If the player rolls this dice, he/she will win: %d\n",total);

		break;

	}



	while(gamestate == 0){

		total = RollingtheDice( );

	if(total == playerrating)

		gamestate = 1;

	else

		if(total == 7)

			gamestate = 2;

	}

	if(gamestate == 1)

		printf("Player won.");

	else

		printf("Player lost.");

	return 0;

}

```