# Country-Population-Dictionary-Management

population = {
'china' : 143,
'india' : 136,
'usa' : 32,
'pakistan' : 21
}
def add():
country = input("Enter country name to add: ")
country = country.lower()
if country in population:
print("Country already exist in our dataset. Terminating")
return

    p = input(f"Enter population of {country}: ")
    p = float(p)
    population[country] = p
    print_all()

def remove():
country = input("Enter country name to remove:")
country = country.lower()
if country not in population:
print("Country doesn't exist in our dataset. Terminating")
return
del population[country]
print_all()

def query():
country = input("Enter country name to query: ")
country = country.lower()
if country not in population:
print(f"country doesn't exist in our dataset. Terminated")
return
print(f"Population of {country} is: {population[country]} crore")

def print_all():
for country, p in population.items():
print(f"{country} ==> {p}")
def main():
user = input("What do you want: ")
if user.lower() == 'add':
add()
elif user.lower() == 'remove':
remove()
elif user.lower() == 'query':
query()
elif user.lower() == 'print':
print_all()
if **name** == '**main**':
main()
