# M-todos-de-ordenamiento
# Métodos de ordenamiento de algoritmos
Son un conjunto de instrucciones que toman un arreglo o lista como entrada y organizan los elementos en un orden particular.

## Insertion Sort 
Este procedimiento recibe el arreglo de datos a ordenar y altera las posiciones de sus elementos hasta dejarlos ordenados de menor a mayor. 
```javascript
public class InsertionSortExample {  
    public static void insertionSort(int array[]) {  
        int n = array.length;  
        for (int j = 1; j < n; j++) {  
            int key = array[j];  
            int i = j-1;  
            while ( (i > -1) && ( array [i] > key ) ) {  
                array [i+1] = array [i];  
                i--;  
            }  
            array[i+1] = key;  
        }  
    }  
    public static void main(String a[]){    
        int[] arr1 = {9,14,3,2,43,11,58,22};    
        System.out.println("Before Insertion Sort");    
        for(int i:arr1){    
            System.out.print(i+" ");    
        }    
        System.out.println();    
            
        insertionSort(arr1);//sorting array using insertion sort    
           
        System.out.println("After Insertion Sort");    
        for(int i:arr1){    
            System.out.print(i+" ");    
        }    
    }    
}    
```
![download](https://github.com/alelomelir/M-todos-de-ordenamiento/assets/160270480/ee38580d-a74b-4a56-8a1d-b6a5d8fa0aaa)

## Selection Sort
Este método consiste en encontrar el menor de todos los elementos de arreglo e intercambiarlo con el que está en la primera posición, luego el segundo más pequeño y así sucesivamente hasta ordenar todo el arreglo.
```javascript
public class SelectionSortExample {  
    public static void selectionSort(int[] arr){  
        for (int i = 0; i < arr.length - 1; i++)  
        {  
            int index = i;  
            for (int j = i + 1; j < arr.length; j++){  
                if (arr[j] < arr[index]){  
                    index = j;//searching for lowest index  
                }  
            }  
            int smallerNumber = arr[index];   
            arr[index] = arr[i];  
            arr[i] = smallerNumber;  
        }  
    }  
       
    public static void main(String a[]){  
        int[] arr1 = {9,14,3,2,43,11,58,22};  
        System.out.println("Before Selection Sort");  
        for(int i:arr1){  
            System.out.print(i+" ");  
        }  
        System.out.println();  
          
        selectionSort(arr1);//sorting array using selection sort  
         
        System.out.println("After Selection Sort");  
        for(int i:arr1){  
            System.out.print(i+" ");  
        }  
    }  
}  
```
![download](https://github.com/alelomelir/M-todos-de-ordenamiento/assets/160270480/74831f4d-bbfd-499e-878f-acd498e4dc7c)

## Bubble Sort
Consiste en comparar los dos primeros elementos de la lista, si el primer elemento es mayor que el segundo, se intercambian, si no, se quedan como están. Este proceso de repite hasta que la estructura este ordenada. 
```javascript
public class BubbleSortExample {  
    static void bubbleSort(int[] arr) {  
        int n = arr.length;  
        int temp = 0;  
         for(int i=0; i < n; i++){  
                 for(int j=1; j < (n-i); j++){  
                          if(arr[j-1] > arr[j]){  
                                 //swap elements  
                                 temp = arr[j-1];  
                                 arr[j-1] = arr[j];  
                                 arr[j] = temp;  
                         }       
                 }  
         }  
 }  
    public static void main(String[] args) {  
                int arr[] ={3,60,35,2,45,320,5}; 
                System.out.println("Array Before Bubble Sort");  
                for(int i=0; i < arr.length; i++){  
                        System.out.print(arr[i] + " ");  
                }  
                System.out.println();  
                  
                bubbleSort(arr);//sorting array elements using bubble sort  
                 
                System.out.println("Array After Bubble Sort");  
                for(int i=0; i < arr.length; i++){  
                        System.out.print(arr[i] + " ");  
                }  
   
        }  
}  
```
![images](https://github.com/alelomelir/M-todos-de-ordenamiento/assets/160270480/51572974-a2c0-44c0-8283-c97cbb0e9387)

Alejandra Lomeli Rodriguez 4P 22310413


