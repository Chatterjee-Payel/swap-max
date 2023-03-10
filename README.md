# swap-max
long long int maxSum(int arr[], int n)
{
    vector<int>v;
    sort(arr,arr+n);
    int i = 0;
    int j = n-1;
    while(i<=n)
    {
        v.push_back(arr[i++]);
        v.push_back(arr[j--]);
    }
    long long sum = 0;
    for(int i = 0;i<n-1;i++)
    {
        sum = sum+abs(v[i]-v[i+1]);
    }
    return sum +abs(v[0]-v[n-1]);
    
}
