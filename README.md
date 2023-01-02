# alexis
URBANESE STREAMLIT 
#Bibliothèques 
import streamlit as st 
import pandas as pd
import numpy as np
import time

import requests
import streamlit as st

#Mise en page
st.title('Bienvenue chez :red[URBANEASE]')

#Image
st.image(
            "https://frenchproptech.fr/wp-content/uploads/2021/06/Hub-ProspecImmo-Urbanease.jpg",
            width=400 # Manually Adjust the width of the image as per requirement
        )

#Barre de recherche 
def main():
    # Afficher une barre de recherche pour entrer le code Siren
    siren = st.text_input("Entrez le code Siren de l'entreprise :")

    # Vérifier si le code Siren a été entré
    if siren:
        # Appeler la fonction get_company_info avec le code Siren entré
        company_info = get_company_info(siren)

        # Afficher les informations de l'entreprise
        st.write(company_info)

if __name__ == "__main__":
    main()

#st.markdown("Projet réalise par l'equipe 'Nom de notre equipe' en colaboration avec Urbanease & La Wild Code School de Lyon")

