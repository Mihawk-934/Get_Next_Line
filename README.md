# Get_Next_Line 

Ce projet est le projet de démarrage final avant de se diversifier. L'objectif est de créer une fonction qui lit une seule ligne à partir d'un descripteur de fichier, en supposant qu'elle n'est pas falsifiée entre les appels à la fonction.

Il doit tenir dans un fichier source et un en-tête. Le mien fonctionne avec plusieurs descripteurs de fichiers. Il n'a également aucune fuite de mémoire (hourra)!

## Usage
```c
char * line;

// Pour obtenir une seule ligne 
get_next_line (fd, & line);
...
ft_strdel (& line); // Vous devriez libérer après avoir utilisé votre ligne

// Pour lire un fichier entier 
while (get_next_line (fd, & line))
{
    // traite la ligne ici, ici nous allons juste la sortir 
    ft_putstr (ligne);

    // libère la ligne pour éviter les fuites de mémoire 
    ft_strdel (& line);
}

// GNL sera automatiquement libéré de manière appropriée chaque fois qu'il atteindra EOF.
```
