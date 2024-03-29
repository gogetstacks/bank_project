children_grouped = data.groupby('children')['children'].count()
def child_group(debt):
    try:
        debt = data['debt']
        children = data['children']
        if debt == 1:
            if children == 1:
                return one_child_part
            if children == 2:
                return two_child_part
            if children == 3:
                return three_child_part
            if children == 4:
                return four_child_part
            if children == 5:
                return five_child_part
    except:
        return 'ошибка'

            
children_grouped['children_debt'] = data['children'].apply(child_group, axis=1)
children_grouped# bank_project
