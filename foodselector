#!/usr/bin/env python3
import argparse
import random

def cuisine_choices() -> dict[str : str]:

    cuisine = {}
    cuisine['Pizza'] = ['Pizza Hut',
                        'Dominoes',
                        'California Pizza', 
                        'Sarpinos',
                        'Papa Johns',
                        'NY 212',
                        'Pizza Max',
                        'Broadway',
                        'Manhattan Bites',
                        'Pizzaria',
                        'Cheese Factor']

    cuisine['Steak'] = ['Arcadian',
                        'Gunsmoke',
                        'Wasabi',
                        'Howdy',
                        'Bovinoes Steakhouse',
                        'Ox and Grill Steakhouse',
                        'Texas Grill',
                        'Sumo',
                        'London Courtyard']

    cuisine['Burger'] = ['Mc Donalds',
                        'Hardies',
                        'KFC',
                        'Burger King',
                        'Howdy',
                        'Daily Deli']

    cuisine['Pasta'] = ['PF Changs']

    cuisine['Sushi'] = ['Saku Hana',
                        'PF Changs',
                        'Wasabi',
                        'Sumo',
                        'Gaia Japanese Fusion Restaurant']

    cuisine['BBQ'] = ['BBQ Tonight',
                    'Faaiqs House']
    
    cuisine['Chinese'] = ['Rice Bowl',
                        'Yum',
                        'Kim Mun',
                        'Sichuan',
                        'PF Changs']

    return cuisine
    
def random_cuisine(cuisine: dict[str : str]) -> str:
    return random.choice(cuisine[random.choice(list(cuisine.keys()))])

def main():
    parser = argparse.ArgumentParser(description='Select a cuisine and restaurant at random for when you are unsure')
    parser.add_argument('-c', metavar='CUISINE', action='store', type=str, help='Specify a cuisine')
    parser.add_argument('-l', action='store_true', help='List all cuisines')
    args = parser.parse_args()

    cuisine = cuisine_choices()

    if args.l:
        for key in cuisine:
            print(key)
    
    if not args.l:
        if args.c:
            if args.c in cuisine:
                print(random.choice(cuisine[args.c]))
            else:
                print('No such cuisine')
        elif not args.c:
            print(random_cuisine(cuisine))


if __name__ == '__main__':
    main()