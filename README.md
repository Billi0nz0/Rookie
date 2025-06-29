print ("Welcome to Naija Recipes")

def greet_user(username):
  return f"Hello {username}, What receipe are you looking for today?"
username = "Victoria"
greeting = greet_user(username)
print (greeting)

def search_feature():
  Query = input("Enter the name of the recipe you are looking for:")
  return f"searching for {Query}"

recepies = [
  {
    "name": "Nigerian Jollof Rice",
    "INGREDIENTS": [
    "FOR THE BASE",
      "1 large red bell pepper, cut into small pieces",
      "2 medium vine tomatoes, cut into small pieces",
      "1 red onion, quartered",
      "2 red scotch bonnet chillies, quartered",
      "3 garlic cloves, smashed",
      "25g fresh ginger, peeled and roughly chopped",
      "100ml water",
    "FOR THE RICE",
      "150ml vegetable oil.",
      "1 red onion, finely chopped.",
      "150g double concentrated tomato purée (we use GINO).",
      "1 tbsp curry powder.",
      "2 tsp dried thyme.",
      "3 chicken stock cubes.",
      "2 dried bay leaves.",
      "600ml water.",
      "600g white basmati rice or any rice of your choice."
    ],
    "HOW TO PREPARE IT": [
      "Place the base ingredients in a blender and blitz until smooth.",
      "Heat the vegetable oil in a large Dutch oven set over a medium heat. Add the onion and cook, stirring occasionally, for 3 minutes, then add the tomato purée and cook, stirring frequently, until it begins to darken, 3 to 5 minutes.",
      
      "Pour in the blended base, stir to combine and bring to a simmer. Reduce the heat to medium-low and partially cover the pot with the lid – it will splatter! Cook, stirring occasionally, until the sauce is reduced by about a third of its original volume and the oil begins to separate from the sauce, 12 to 15 minutes.",
      
      "Stir in the curry powder, thyme, stock cubes, bay leaves and water. Season generously with salt and pepper, to taste, then cover and bring to a boil over medium-high heat." "Stir in the curry powder, thyme, stock cubes, bay leaves and water. Season generously with salt and pepper, to taste, then cover and bring to a boil over medium-high heat.",
      
      "Meanwhile, rinse the rice thoroughly with cold water until the water runs clean, then drain. Add the rice to the sauce and stir to combine. As soon as it comes to a boil, reduce the heat to low, cover the pot and cook for 25 minutes.",
      
      "By this point, the rice should have absorbed all the liquid and be cooked through. Remove the bay leaves, give the rice a stir and you’re ready to serve, preferably with grilled chicken and fried plantain."
    ]
  }             
]                

def display_recipe(recipe_name, recipes):
  for recipe in recipes:
    if recipe["name"] == recipe_name:
      print(f"\nRecipe: {recipe['name']}")
      print("\nIngredients:")
      for ingredient in recipe["INGREDIENTS"]:
        print(f"- {ingredient}")
      print("\nInstructions:")
      for step in recipe["HOW TO PREPARE IT"]:
        print(f"- {step}")
    elif recipe["name"] != recipe_name:
        print ("Recipe not found")

Query_result = search_feature()
display_recipe(Query_result.replace("searching for ", ""), recepies)
print ("Thank you for using Naija Recipes")
