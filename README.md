# hw4
public class hw4{
    public static void main(String[] args) {
        double in[] = new double[]{45, 15, -1, 79, 89, 52, 66, 33, 56, 105};
        isStrictlyIncreasing(in);
        
            System.out.println("Answer: " + isStrictlyIncreasing(in));
        
    }
    private static boolean isStrictlyIncreasing(double[] in) {
        int n = in.length;
        for(int i = 1; i < n-1; i++){
            if(in[i - 1] < in[i]){
                return true;
         }
        }return false;
  }
}


public class hw4pt2{
    public static char[] removeDuplicates(char[] in) {
        int[] ch=new int[in.length];
        int ind=0;
        int co=0;
        for(int i=0;i<in.length;i++){
            ch[i]=1; 
        }
        for(int i=0;i<in.length;i++){
            if(ch[i]!=0){
                for(int j=i+1;j<in.length;j++){
                    if(in[i]==in[j]){
                        ch[j]=0;
                    }
                }
            }
        }
        for(int i=0;i<in.length;i++){
            if(ch[i]==1){
                co++;}
            }
        char[] result=new char[co];
        for(int i=0;i<in.length;i++){
            if(ch[i]==1){
                result[ind]=in[i];
                ind++;
            }
        }
        return result;
    }
    public static void main(String[] args){
        char str[] = {'b', 'd', 'a', 'b', 'f', 'a', 'g', 'a', 'a', 'f'};
        int n = str.length;
        System.out.print("Input: ");
        for(int i=0;i<n;i++){
            System.out.print(str[i]+",");
        }
        System.out.println();
        System.out.print("Output: ");
        char str2[]=removeDuplicates(str);
        n = str2.length;
        for(int i=0;i<n;i++){
            System.out.print(str2[i]+",");
        }
    }
}




public class hw4pt3 {
    static int[] remove(int v, int[] in){
        int i, count = 0;
        for(i = 0;i<in.length;i++){
            if(in[i] == v){
                count++;
            }
        }
        int out[] = new int[in.length-count];
        int k = 0;
        for(i = 0;i<in.length;i++){
            if(in[i]!=v){
                out[k++] = in[i];
            }
        }
        return out;
    }

    public static void main(String args[]){
        int in[] = {0, 1, 3, 2, 3, 0, 3, 1};
        int v = 3;
        int out[] = remove(v,in);
        System.out.println("Array ofter remove all "+v +": ");
        for(int i = 0;i<out.length;i++){
            System.out.println(out[i]);
        }
    }
}


public class hw4pt4 {
static int[] combineOrder(int arr1[],int arr2[]){
int arr[] = new int[5];
for(int i = 0;i<5;i++){
arr[i] = arr1[i] + arr2[i];
}
return arr;
}

public static void main(String args[]){
int arr1[] = {0, 0, 3, 4, 7};
int arr2[] = {0, 4, 0, 1, 2};

int[] arr = combineOrder(arr1,arr2);
System.out.println("Combined order: ");
for(int i = 0;i<5;i++){
System.out.println(arr[i]);
}
}
}

