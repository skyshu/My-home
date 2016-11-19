# My-home
sky's home page
  class search_bin
    {
        private static search_bin s;
        public static search_bin S
        {
            get
            {
                if (s == null)
                    s = new search_bin();
                return s;
            }
        }
        public int search(double[] a, int len,double score)
        {
            int low = 1,mid;
            while (low <= len)
            {
                mid = (low + len) / 2;
                if (a[mid] == score)
                    return mid;
                else if (a[mid] < score)
                    len = mid - 1;
                else
                    low = mid + 1;
            }
            return 0;
        }
    }
