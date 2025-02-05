The create_family function takes an integer (generations) as input and allocates (as via malloc) one person for each member of the family of that number of generations, returning a pointer to the person in the youngest generation.
For example, create_family(3) returns a pointer to a person with two parents, where each parent also has two parents.
Each person has alleles assigned to them. The oldest generation has alleles randomly chosen (as by calling the random_allele function), and younger generations inherit one allele (chosen at random) from each parent.
Each person has parents assigned to them. The oldest generation has both parents set to NULL, and younger generations have parents as an array of two pointers, each pointing to a different parent.
