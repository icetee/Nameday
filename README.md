## Névnap ##

### Használat ###
Ahogy az example.php fájlban is megtalálható, egy új objektumot kell létrehozni, hogy hívatkozni lehessen az osztályra.

======

Ehhez először meg kell hívni az osztályt tartalmazó fájlt:

    require_once 'nevnap-class.php';


Majd csak ezútán lehet létrehozni az új objektumot:

    $nevnap = new Nevnap();

A jelenlegi dátum lekérdezés így lehetséges:

    print $nevnap->getDate();

A jelenlegi névnap kiírása pedig így történik:

    $nevnap->getNevnap();

Van lehetőség arra is, hogy ne az összes névnapos jelenjen meg, hanem csak korlátozott létszámban:

    $nevnap->getNevnap(3);

Amennyiben nem a mai névnaposokat akarjuk kiírni, akkor adjunk meg egy dátumot, majd a névnapok újra lekérdezésével frissülnek a névnapok.

    $nevnap->reDate("2016-02-24");
    $nevnap->getNevnap();

## Name day ##

### Use ###

As you can see in example.php, a new object is need to be created in order to refer to the class.

======

First of all we have to call the file conatining the class.

    require_once 'nevnap-class.php';

And only after this, a new object can be created.

    $nevnap = new Nevnap();

The current nameday can be queried with this code:

    print $nevnap->getDate();

And you can write/display the current name day with this code:

    $nevnap->getNevnap();

It is possible to limit the amount of the displayed names.

    $nevnap->getNevnap(3);

If we want to display an other date's names, we give the required date, and the names refresh after a new query.

    $nevnap->reDate("2016-02-24");
    $nevnap->getNevnap();
