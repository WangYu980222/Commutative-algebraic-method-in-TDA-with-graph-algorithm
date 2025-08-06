# Commutative-algebraic-method-in-TDA-with-graph-algorithm
This program consists of an algorithm to use commutative algebraic methods in Topological Data Analysis with graph theorem (and without computational commutative algebra).  The algorithm will be applied for Viectoris-Rips complex and use the commutative algebraic method according to Stanley-Reisner ideals. The algorithm is based on the language Python and it only needs the basic packages like numpy.
Here is the list of functions which are included in this algorithm and there corresponding usage.
persistence_barcode(births, deaths, ideallist)：produces a diagram of persistence barcodes of persistent ideals with the input of list of birthtime (births), deathtime (deaths) and the associated primes (idealist). Remember that the order of index of the three list should be in correspondence.
generate_parameter_name_list(input_indices): produces a list of radical monomial ideals according to the list of indices (input_indices).
all_maximal_cliques(G): produces a list of all maximal cliques with the given graph (G). 
next_maximal_clique(G, C, P, S, cliques):  a recursive program produces a maximal clique according to the vertex set (G,C,P,S). The result is stored in the list (cliques). 
select_pivot(G, P, S): selects a pivot vertex from P ∪ S to maximize |P ∩ neighbors(pivot). This helps minimize recursive calls.
gram_matrix_to_ordered_array(gram_matrix): produces an ordered array (from small to large) of the entries of a given symmetric matrix (gram_matrix).
gram_matrix_to_viectoris_rips(gram_matrix, threshold): gets a Viectoris-Rips complex from a distance matrix (gram_matrix) and a radius threhold (threshold)
gram_matrix_to_persistent_viectoris_rips(gram_matrix, thresholds): gets persistent Viectoris-Rips complexes from a distance matrix (gram_matrix) and a list of radius threhold (thresholds)
calculate_associative_primes(Cliques, datapoints): gets the set of associated prime of the Stanley-Reisner ideal from the set of maximal cliques (Cliques) of its corresponding graphs. Here the set (datapoints) is a set $\{1,\dots,n\}$ which represents the set of vertices the graphs on. Note that this algorithm only applies to the clique complex of a graph.
calculate_birth_death_times(persistent_complexes, timeseries, data_points): calculates the birth and death time of a the persistent ideals according to a persistent Viectoris-Rips complex (persistent_complexes) on the vertex set (data_points) and a given radius/time series (timeseries) 
calculate_gram_matrix(datapoints): calculates the distance matrix of a given set of data points (datapoints) in the Euclidean space
