Le changement climatique est une réalité incontestable qui affecte notre quotidien. 
Le réchauffement de la France est déjà de +1,7°C  par rapport aux années 1850. Si on ne change rien, la trajectoire actuelle amène le monde vers une élévation des températures à +3°C en 2100 ce qui signifie, par exemple, + 4°C pour le territoire français. 
Quel que soit la géographie, les conséquences pour la vie humaine sont considérables. Les causes du réchauffement climatiques sont globalement communes avec celles de l’augmentation de la pollution.
En effet, les émissions de GES, telles que le dioxyde de carbone (CO2), le méthane (CH4) et le protoxyde d'azote (N2O), sont des facteurs majeurs de la pollution atmosphérique et du changement climatique. 
Les émissions mondiales de CO2, principalement dues à la combustion de combustibles fossiles, ont augmenté de manière significative au cours des dernières décennies, contribuant ainsi au réchauffement climatique. 
La pollution de l'air, principalement causée par les émissions des véhicules, des centrales électriques, de l'industrie et d'autres sources, est un problème majeur dans de nombreuses régions du monde. Les particules fines, les oxydes d'azote, le dioxyde de soufre et d'autres polluants atmosphériques peuvent avoir des effets néfastes sur la santé humaine et l'environnement. 
Le consensus qui est en train de s’établir auprès de toutes les parties prenantes est qu’il est nécessaire de s’adapter et d’atténuer significativement les émissions de CO2 et de polluants. 
« S’adapter » signifie réduire notre vulnérabilité face aux impacts du changement climatique (protection des personnes, préparation des territoires, préservation des milieux naturels et du patrimoine culturel…).
« Atténuer » signifie diminuer nos impacts dont, entre autre, réduire les polluants et les émissions de gaz à effet de serre d’origine anthropique. 
L’effet de serre en lui-même n’est pas problématique, puisque c’est grâce à ce mécanisme physique que les conditions de vie humaine sont possibles sur Terre. 
C’est l’excès croissant de CO2 généré par les activités humaines depuis 150 ans qui est alertant. En effet, il induit un forçage radiatif qui concentre des gaz à fort pouvoir réchauffant. Le réchauffement climatique induit des conséquences trop impactantes pour le vivant. Il s’agit donc d’un enjeu essentiel à traiter. 
Force est de constater que le secteur des transports a de lourds impacts environnementaux. 
Et pour cause, en prenant l’exemple de la France, il fait partie des principaux émetteurs de gaz à effet de serre (GES) dont le dioxyde de carbone (CO2). 
Selon les chiffres de l’Agence de l’Environnement et de la Maîtrise de l’Énergie (Ademe) datant d’avril 2018, les transports sont responsables de 39 % des émissions totales de gaz à effet de serre dans le pays. 
Dans le détail, plus de la moitié de ces émissions sont produites par les voitures, 20 % des GES sont émis par les poids lourds, et 17 % par les petits véhicules utilitaires. La part restante concerne les deux-roues, les avions et les transports ferroviaires, maritimes et fluviaux. La quasi-totalité des émissions de gaz à effet de serre (93 %) est liée au transport routier. 
Un chiffre qui n’a rien de surprenant puisque près de neuf trajets sur dix, en France, sont réalisés en voiture (particuliers et professionnels confondus). De même, 90 % du transport de marchandises du pays se réalise via les différents axes routiers.
Parmi les actions pour mettre en route rapidement la trajectoire d’atténuation, il est nécessaire d’identifier les véhicules qui émettent le plus de CO2 pour comprendre les caractéristiques techniques qui jouent un rôle dans la pollution.
Prédire cette pollution permet de prévenir dans le cas d’apparition de nouveaux types de véhicules (nouvelles séries de voitures par exemple).

Nous sommes sur un marché qui évolue constamment et cela est d’autant plus nécessaire qu’en 2035, l’Europe a pris un engagement de ne plus vendre les véhicules qui émettent de CO2. 
Ce sera donc un contexte d’amélioration continue pour lequel la précision des mesures sera clef. Il est donc essentiel de choisir un modèle qui soit suffisamment sensible à toutes les améliorations/optimisations apportées par les constructeurs et qui s’adapte à de nouvelles données.
Notre dataset (data_target13.csv) retenu pour l’étude après nettoyage pour la modélisation est constitué de 70366 entrées et de 8 variables dont 7 explicatives et 1 variable cible (CO2) à prédire. 
D’un point de vue technique et malgré différentes méthodes d’optimisation de classification, nous observons toujours le phénomène de surapprentissage dans le modèle de classification dû notamment au déséquilibre de chacune des classes de la variable.
D’un point de vue métier, le choix d’un modèle de classification permettait de simplifier et de faciliter la lecture par tranche d’émission de CO2 pour les véhicules sur le marché. 
Or notre variable cible, l’émission de CO2, est une variable continue qui, au regard des enjeux structurants de réduction, a besoin d’être analysée plus finement et actualisée régulièrement. 
Mettre un nouveau référentiel de classes qui serait susceptible d’être à nouveau modifié pourrait provoquer l’incompréhension du grand public. Aussi, mesurer l’émission sur des tranches de catégories limite aussi la précision de la mesure de l’impact.
C’est pour cela que nous avons souhaité élargir notre étude aux modèles de Regressor.
Nous choisissons finalement parmi les 3 Regressors le modèle Random Forest Regressor pour la modélisation de ML qui apporte une excellente précision et un surapprentissage le plus faible parmi les modèles les plus performants analysés. 
Notre choix s’accompagne d’une recommadation de mise en oeuvre d’une stratégie intégrant les éléments clefs cités ci-dessus pour assurer la bonne adaptation au marché changeant.
Nous avons développé une application sur Streamlit qui permet de prédire la valeur de l’émission de CO2 en rentrant les données des caractéristiques telles que le Poids, la Puissance, la Dimension, le Cylindrée, l’Autonomie-électrique, le Fuel mode et le Fuel type.





